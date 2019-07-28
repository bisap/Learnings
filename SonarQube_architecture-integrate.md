<b>Integration> </b>

1.	Developers code in their IDEs and use SonarLint to run local analysis.
2.	Developers push their code into their favourite SCM : git, SVN, TFVC, ...
3.	The Continuous Integration Server triggers an automatic build, and the execution of the SonarScanner required to run the SonarQube analysis.
4.	The analysis report is sent to the SonarQube Server for processing.
5.	SonarQube Server processes and stores the analysis report results in the SonarQube Database, and displays the results in the UI.
6.	Developers review, comment, challenge their Issues to manage and reduce their Technical Debt through the SonarQube UI.
7.	Managers receive Reports from the analysis. Ops use APIs to automate configuration and extract data from SonarQube. Ops use JMX to monitor SonarQube Server.

<b>About Machines and Locations</b>
•	The SonarQube Platform cannot have more than one SonarQube Server and one SonarQube Database.
•	For optimal performance, each component (server, database, scanners) should be installed on a separate machine, and the server machine should be dedicated.
•	SonarScanners scale by adding machines.
•	All machines must be time synchronized.
•	The SonarQube Server and the SonarQube Database must be located in the same network
•	SonarScanners don't need to be on the same network as the SonarQube Server.
•	There is no communication between SonarScanners and the SonarQube Database.

