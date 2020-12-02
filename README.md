# How-to-install-Jenkins-on-Ubuntu-
Installing Jenkins on Ubuntu Server in AWS 

After logging into Ubuntu Server 
#Perform update 
sudo apt update

#Install Java 8
sudo apt install openjdk-8-jdk -y

#Verify Java Version
java -version

#Maven Installation

sudo apt install maven -y

# then type
 mvn --version


#Jenkins Setup

#Add Repository key to the system 


wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -

#Append debian package repo address to the system

echo deb http://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list

sudo apt update

#Install Jenkins
sudo apt install jenkins -y

#Access Jenkins in web browser

http://ec2_public_dns_name:8080/

Alternatively,

http://ec2_public-ip:8080/

#Get the password from the below file to unlock Jenkins on browser

sudo cat /var/lib/jenkins/secrets/initialAdminPassword

#Copy the password and paste in the browser.
#Then click on install suggested plug-ins.

#Also create user name and password.
#enter everything as admin. at least user name as admin password as admin

#Click on Save and Finish. Click on Start using Jenkins. 









