1. Install jenkins
 
Pre-Requisites:

Java (JDK)
Run the below commands to install Java and Jenkins
Install Java

sudo apt update
sudo apt install openjdk-11-jre
Verify Java is Installed

java -version
Now, you can proceed with installing Jenkins
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
**Note: ** By default, Jenkins will not be accessible to the external world due to the inbound traffic restriction by AWS. Open port 8080 in the inbound traffic rules as show below.

2. Install sonarqube -
   sudo docker container run -dt --name sonarqube -p 9000:9000 sonarqube
Default credentials admin & admin



