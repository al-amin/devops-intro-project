# How to Install tomcat

1. Download latest tomcat server from http://tomcat.apache.org
2. To install the tomcat server we gonna need java 8 +
3. Just extract the zip file in any location
4. Then inside that folder, we will find "bin" directory
	- There we need to make all the `.sh` files executable. 
	- To see all the executable files mac command is `ls -al *.sh`
	- To make executable all the .sh files mac command is - `sudo chmod +x *.sh`

5. To **RUN** tomcat server - `./startup.sh`
6. To **CHECK** server running or not visit into the browser: `localhost:8080`
7. To **STOP** tomcat server - `./shutdown.sh`


# How to Install Jenkins

1. Download latest Jenkins server from https://jenkins.io/download/
2. We downloaded Generic Java package (.war)
3. Open up a terminal in the download directory
4. Run `java -jar jenkins.war --httpPort=8080`
5. Browse to http://localhost:8080
	- Follow the instructions to complete the installation
	- It gonna ask for admin pass and show a file location on the computer, from where you can get admin password `(/Users/XXXXX/.jenkins/secrets/initialAdminPassword)`
	-	It will suggest for plugins selection - optional

# How to run Jenkins server on tomcat server

1. First we need to **stop** tomcat server using this command `./shutdown.sh`
2. For this we need to copy `jenkins.war` file into the `tomcat/webapps` folder
3. Then we need to start our tomcat server using this command - `./startup.sh`
4. Then we need to visit `localhost:8080/jenkins`
5. We need to give the admin password from the previous location `(/Users/XXXXX/.jenkins/secrets/initialAdminPassword)`