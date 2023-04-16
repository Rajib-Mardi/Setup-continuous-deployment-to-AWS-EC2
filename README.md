# AWS-Services

## Demo Project:
*  CD - Deploy Application from Jenkins Pipeline to EC2 Instance (automatically with docker)

## Technologiesused:
*  AWS, Jenkins, Docker, Linux, Git, Java, Maven, Docker Hub

Demo 1 executed - Deploy WebApp Container via Jenkins Pipeline on EC2 Instance:

* Installed SSH agent plugin on Jenkins

![Available plugins - Plugin Manager  Jenkins  - Google Chrome 14-04-2023 11_12_28](https://user-images.githubusercontent.com/96679708/232266677-8fef5acc-0b91-4ea7-81d0-d511071934d5.png)


* Created ssh credentials type for EC2 on Jenkins
![my-multi-branch-pipeline » Folder » Global credentials (unrestricted)  Jenkins  - Google Chrome 16-04-2023 10_00_22](https://user-images.githubusercontent.com/96679708/232266723-1395008c-5ed7-47f8-9683-1085759f9713.png)


*  Configured Jenkinsfile to use the sshAgent and execute docker run command 
on EC2

  
  
  
*  Docker Login to DockerHub or your other private Docker Repository (if you haven’t already)
*  Security Group configured: Added Jenkins IP Address and opened port to access Web App from Browser
* Deploy Webapp on EC2 Instance by executed Multi-Branch Pipeline
*  Access Application on port 3080 in the browser
