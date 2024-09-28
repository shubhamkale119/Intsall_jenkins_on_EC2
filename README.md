## Install_jenkins_on_EC2 Amazon Linux

- Launch EC2 instance first and connect it using SSH

## Commands to Install And run Jenkins

- Update preinstalled library
  
  ``` sudo yum update ```

- Add the Jenkins repo using the following command:
  
      sudo wget -O /etc/yum.repos.d/jenkins.repo \ 
      https://pkg.jenkins.io/redhat-stable/jenkins.repo 

- Import a key file from Jenkins-CI to enable installation from the package:

      sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key 
      sudo yum upgrade`

- Install Java (Amazon Linux 2023):
  
      sudo dnf install java-17-amazon-corretto -y 

- Install Jenkins:
  
      sudo yum install jenkins -y

- Enable the Jenkins service to start at boot:
  
      sudo systemctl enable jenkins

- Start Jenkins as a service:
  
      sudo systemctl start jenkins

- Add security group as 8080 port with EC2 instance in the security policy


## Jenkins is master slave architecture  so how to coonect master with slave

  - Create one serever where your jenkins has already installed
  - Create another server where your slave is there with Java
  - Create public and private key in the .ssh folder with command keygen
  - Please refert this video link: https://youtu.be/XaSdKR2fOU4?si=qfzOIlusd-SyW4cu
