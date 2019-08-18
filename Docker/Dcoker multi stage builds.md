<ul>
  <li>With multi-stage builds, you use multiple FROM statements in your Dockerfile. Each FROM instruction can use a different base, and each of them begins a new stage of the build. You can selectively copy artifacts from one stage to another, leaving behind everything you don’t want in the final image,The end result is the same tiny production image as before, with a significant reduction in complexity</li>
  <li> Only runtime artifacts that we need from our previous  stages</li>  
</ul>
