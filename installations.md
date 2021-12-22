JAVA 8 installation in ubuntu 16.04:
sudo apt-get -y install default-jdk


Java 11 ( open JDK ):
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt install openjdk-11-jdk


JAVA 11 installation in ubuntu 16.04:
sudo add-apt-repository ppa:linuxuprising/java
sudo apt update
sudo apt-get install oracle-java11-installer
sudo apt-get install oracle-java11-set-default ( to set java 11 as default )
java -version ( verify java installation )
for more details - https://tecadmin.net/install-oracle-java-11-on-ubuntu-16-04-xenial/


JAVA 11 installation in GCP machine:
download jdk-11.0.12_linux-x64_bin.tar.gz from https://www.oracle.com/java/technologies/downloads/#java11 and place it under /var/cache/oracle-jdk11-installer-local
sudo apt-get install oracle-java11-installer-local
sudo apt install oracle-java11-set-default-local


git installation in ubuntu 16.04:
apt-get update
apt-get install git
git --version ( to verify git version )


Jenkins installation in ubuntu 16.04:
wget https://updates.jenkins-ci.org/download/war/2.162/jenkins.war ( installs 2.162 version, if you want any other version to be installed visit https://updates.jenkins-ci.org/download/war/ download particular version )
java -jar jenkins.war ( default runs on 8080 port )
java -jar jenkins.war --httpPort=5000 ( if you want run on any other port use this, in my case its 5000 port )
nohup java -jar jenkins.jar & ( to run jenkins process in background )


Jenkins as a service:
wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
echo deb https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list
apt-get update
apt-get install jenkins
systemctl start jenkins
systemctl status jenkins









