# AWS-3-Tier
Deploy AWS 3-Tier infrastructure with Terraform, Ansible, Terragrunt Jenkins pipeline integration

- Infrastructure
![sanjo](https://github.com/Sanjo-varghese/AWS-3-Tier/assets/116708794/1a6813cb-54a0-48fd-9895-1e5f1dc213f0)

# Platform Setup
  Login to aws Mangement console
  - create a ec2 instance
  - Name :web app
  - Ami :Amazon linux 2
  - Instance type :t2.micro
  - key pair (login) :sanjo.pem
  - vpc :default
  - launch instance
- Login via Mobaxtrem or putty

  #AMAZON LINUX 2 AMI
  
  ``sh
  sudo su -
  ``
  -Install nginix on amazon linux
  
  ``sh
  amazon-linux-extras install nginx1
  ``
  -start the service
  
  ``sh
  systemctl enable nginx
  ``
  -install awscli
  
  ``sh
  yum install awscli
  ``
  -Install ansible Package
  
  ``sh
  amazon-linux-extras install ansible2 -y
  ``
  -install amazon ssm-agent
  
  ``sh
  yum install amazon-ssm-agent
  ``
  
  # Take a copy of AMI of ec2 server
   - ec2 management console -> actions -> image and templates -> create image -> 
   - image name :sanjo-webami
   - create image
     
   # create a Tomcat server to run App
  - Ec2 management console
  - Name :App-server
  - AMI :AMAZON LINUX 2
  - Instace type :t2.micro
  - key pair :sanjo.pem
  - VPC :Default
  - launch instance

     login via ssh
 - Navigate to super user
   
   ``sh
sudo su -
``
- install jdk packages 8
  ``sh
  yum install java-1.8.0-openjdk-devel -y
  ``
  - install ansible packages
    ``sh
    amazon-linux-extras install ansible2 -y
    ``
    - install apache tomcat
    - visit - https://tomcat.apache.org/download-80.cgi
    - cd /opt
    - wget https://downloads.apache.org/tomcat/tomcat-8/v8.5.95/bin/apache-tomcat-8.5.95.tar.gz.sha512
      
      unzip 
   
  ``sh
  tar -zxvf apache-tomcat-8.5.95.tar.gz
  ``
   rename tocat
  ``sh
  mv apache-tomcat-8.5.95 tomcat
  ``
  - cd tomcat
  - pwd
  - 
    Take a copy of AMI of tomcat-ec2 server
   - ec2 management console -> actions -> image and templates -> create image -> 
   - image name :sanjo-app-ami
   - create image
    
  
  
  
     
