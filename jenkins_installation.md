# Installing Jenkins

## Install Java
````bash
apt install openjdk-8-jdk
````

## Install Jenkins
````bash
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
    /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
````

## Finish installation
1. Browse to <ip_address>:8080
2. Follow onscreen instructions
