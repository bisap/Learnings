What is LDAP?
LDAP (Lightweight Directory Access Protocol) is an open and cross platform protocol used for directory services authentication.

LDAP provides the communication language that applications use to communicate with other directory services servers. Directory services store the users, passwords, and computer accounts, and share that information with other entities on the network.

<b>What is Active Directory?</b>
Active Directory is a directory services implementation that provides all sorts of functionality like authentication, group and user management, policy administration and more.

LDAP vs. Active Directory
LDAP is a way of speaking to Active Directory.

LDAP is a protocol that many different directory services and access management solutions can understand.

The relationship between AD and LDAP is much like the relationship between Apache and HTTP:

HTTP is a web protocol.
Apache is a web server that uses the HTTP protocol.
LDAP is a directory services protocol.
Active Directory is a directory server that uses the LDAP protocol.

LDAP is a protocol, and Active Directory is a server. LDAP authenticates Active Directory – it’s a set of guidelines to send and receive information (like usernames and passwords) to Active Directory. 

<b>Use Cases :</b>
You're developing an in-house application for your company and the app might need employee details such as name, employee ID, position etc.. for various reasons. There would be constant querying (READ) operation to LDAP to retrieve the information.

You might ask why Database can't be used. It highly depends on the use case. If there's more READ operation and you need to store information such as roles, permissions of the user, LDAP store it in the tree structure. If frequent updates and inserts are essential, then choose database over LDAP as it's the ideal way.

LDAP is predominantly used application protocol for authentication purposes.

Therefore, use LDAP if there are frequent reads and choose database if there are frequent updates and inserts happening in the application.

<b>Directory Services - An Introduction</b>

A directory service is a centralized, network-based repository that stores and provides access to information that must either be shared between applications or is highly distributed. Directory services play a vital role in developing intranet and Internet applications by helping you share information about users, systems, networks, services, and applications throughout the network

For instance, e-mail systems include directories to store user information and to route messages between senders and receivers. Large corporations also use directories of various forms as repositories of employee information: centrally storing names, departments, managers, social security numbers, and other organizational information.

All Internet applications have a common problem: how to centralize information in a single repository from which it can be efficiently accessed and shared by users or applications. The solution is Directory Services. You can use directory services to store and share a variety of different kinds of information.

Users are represented by their security certificates and their access control privileges, which can be stored centrally in a directory. An administrator then changes the user's information and privileges in a single location rather than making such changes in each of the applications and databases that the user accesses. Additionally, the directory service serves as a central repository to manage distributed network resources

<b>Directory services do this in two ways: <b>

By centralizing the administration of distributed information in a single place
By letting information stored in the directory be easily shared across users and applications within a corporate intranet and across extranets
