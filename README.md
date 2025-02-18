# rvdev 

# rvdev API

# Import Project into eclipse
1.	Select File -> import -> Maven -> Existing Maven Projects
2.	Click Next
3.	Bowese and select the folder
4.	Clink Finish

# MySQL - rvdev Schema (one time setup)
1.	Open MySQL Workbench from Start menu
2.	Click on + next to MySQL connections
3.	In the Setup New Connection screen, enter Connection Name rvdev
-  	Hostname: 127.0.0.1
-   Port: 3306
-   username: root
-   password: root 
4.	Click Ok. “rvdev” will display under  MySQL connections.
5.	Double click on the "rvdev" connection
6.	Open the script rvdev\scripts\rvdev_schema.sql from rvdev project in mysql and execute it.
7. Open the script rvdev\scripts\generic.sql from rvdev project in mysql and execute it.
8. Open the script rvdev\scripts\configuration.sql from rvdev project in mysql and execute it.

# Install Lombok on eclipse (one time setup):
1.	Install lombok jar from https://search.maven.org/search?q=g:org.projectlombok%20AND%20a:lo)mbok&core=gav
2.	Run java -jar lombok-XXX.jar
3.	Installer UI will open. This tries to automatically detect all available Eclipse installations, but it's also possible to specify the location manually.
4.	Once you selected the installations, press the Install/Update button:
5.	Restart eclipse 
6.	If you get build error, Select Project from menu and clean

# Run the application
Run the rvdevApplication.java as Java Application

# Swagger UI: 
In browser open http://localhost:8080/swagger-ui.html

# rvdev UI

# Install Node (one time setup)
Download Windows installer (.msi) from https://nodejs.org/en/download/
Excecute installer from downloads folder
Run following command npm --version in the powershell terminal
If you see the verison number then node installation was successful

# Download Visual Studio Code (one time setup)
Download Visual Studio code from https://code.visualstudio.com/download and install it.

# NPM Install (one-time setup)
Open rvdev-ui in visual studio code
In the terminal, navigate to rvdev-ui folder and run npm install

# Run rvdev UI application
In the terminal, navigate to rvdev-ui folder and run npm start
Open browser and open the url http://localhost:4200/question


# Local Build (single jar)
Open powershell and navigate to rvdev folder

Run command "mvn clean -DskipTests=true install"

# Run application on local server (single jar)

 Run command "java -jar .\rvdev-api\target\rvdev-api-0.0.1-SNAPSHOT.jar" to run the application on local server

In browser, open http://localhost:8080/#/rvdev/login


# Build and deploy to AWS
Open powershell and navigate to rvdev folder
# For Testing environment(https://test.actnowcloud.com)
Run command "mvn clean -DskipTests=true -P=release install"
# For Production environment(https://actnowcloud.com)
Run command "mvn clean -DskipTests=true -P=production install"

Copy rvdev-api-0.0.1-SNAPSHOT.jar from /rvdev/rvdev-api/target to AWS /apps/rvdev/rvdev-api using WinSCP

In putty, navigate to /apps/rvdev/rvdev-api

Run command "sudo su" 

Run command "./restart_rvdevApi" to start the rvdev application.

In browser, open for Testing environment - https://test.actnowcloud.com and 
                    Production Environment https://actnowcloud.com


