<b>Why layers?</b>
<p>
The layers have a couple advantages. First, they are immutable. Once created, that layer identified by a sha256 hash will never change. That immutability allows images to safely build and fork off of each other. If two dockerfiles have the same initial set of lines, and are built on the same server, they will share the same set of initial layers, saving disk space. That also means if you rebuild an image, with just the last few lines of the Dockerfile experiencing changes, only those layers need to be rebuilt and the rest can be reused from the layer cache. This can make a rebuild of docker images very fast.

Inside a container, you see the image filesystem, but that filesystem is not copied. On top of those image layers, the container mounts it's own read-write filesystem layer. Every read of a file goes down through the layers until it hits a layer that has marked the file for deletion, has a copy of the file in that layer, or the read runs out of layers to search through. Every write makes a modification in the container specific read-write layer.
</p>

<b>Reducing layer bloat </b>
<p>
One downside of the layers is building images that duplicate files or ship files that are deleted in a later layer. The solution is often to merge multiple commands into a single RUN command. Particularly when you are modifying existing files or deleting files, you want those steps to run in the same command where they were first created. A rewrite of the above Dockerfile would look like:

FROM busybox

RUN mkdir /data \
 && dd if=/dev/zero bs=1024 count=1024 of=/data/one \
 && chmod -R 0777 /data \
 && dd if=/dev/zero bs=1024 count=1024 of=/data/two \
 && chmod -R 0777 /data \
 && rm /data/one

CMD ls -alh /data
And if you compare the resulting images:

busybox: ~1MB
first image: ~6MB
second image: ~2MB
Just by merging together some lines in the contrived example, we got the same resulting content in our image, and shrunk our image from 5MB to just the 1MB file that you see in the final image.
</p>