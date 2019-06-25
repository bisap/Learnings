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
