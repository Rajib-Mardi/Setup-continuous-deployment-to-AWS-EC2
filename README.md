
### Project:
*  CD - Deploy Application from Jenkins Pipeline to EC2 Instance (automatically with docker)

### Technologiesused:
*  AWS, Jenkins, Docker, Linux, Git, react,nodejs ,Docker Hub

####  Project Description:

###  - Deploy WebApp Container via Jenkins Pipeline on EC2 Instance:



<img src="https://github.com/user-attachments/assets/295230e9-ed62-4fd0-a9eb-6074bf71114b" width="700">

* Create and configure an EC2 Instance on AWS
* Install Docker on remote EC2 Instance

* Install the  Docker on the EC2 instance to containerize the  applications.
* Installed SSH agent plugin on Jenkins


<img src="https://user-images.githubusercontent.com/96679708/232266677-8fef5acc-0b91-4ea7-81d0-d511071934d5.png" width="700">

* Created ssh credentials type for EC2 on Jenkins


<img src="https://user-images.githubusercontent.com/96679708/232266723-1395008c-5ed7-47f8-9683-1085759f9713.png" width="700">

*  Configured Jenkinsfile to use the sshAgent and execute docker run command on EC2 instance



<img src="https://user-images.githubusercontent.com/96679708/232274719-f7d83a74-da83-4771-8a3b-825a0383b6f2.png" width="700">
  
*  Docker Login to DockerHub or your other private Docker Repository (if you haven’t already)
*  Security Group configured: Added Jenkins IP Address and opened port to access Web App from Browser 



<img src="https://user-images.githubusercontent.com/96679708/232274808-a3287246-c6b3-4b30-88b6-4513152076bd.png" width="700">
 
* Deploy Webapp on EC2 Instance by executed Multi-Branch Pipeline


<img src="https://user-images.githubusercontent.com/96679708/232274850-a78db942-89b8-486a-a505-4cbb53db6638.png" width="700">

* as we can see the container is running 



<img src="https://user-images.githubusercontent.com/96679708/232275690-4a390cd7-0d85-4888-8711-f3482a415744.png" width="700">

*  Access Application on port 3080 in the browser




<img src="https://user-images.githubusercontent.com/96679708/232275037-53398831-eca1-409e-862d-4b06376ec119.png" width="800">

-------------------------------------------------------------------

### - Deploy Java Maven App via Jenkins Pipeline on EC2 Instance:



<img src="https://github.com/user-attachments/assets/2e7bab18-ee0f-4f35-907b-d41b5f6bd3bc" width="700">

 * Configured Jenkinsfile to build and deploy on EC2 Instance [Jenkinsfile](https://github.com/Rajib-Mardi/Setup-continuous-deployment-to-AWS-EC2/blob/feature/jenkinsfile-sshagent1/Jenkinsfile)    

   * Extend the previous CI pipeline with deploy step to ssh into the remote EC2 instance and deploy newly built image from Jenkins server
  


<img src="https://github.com/user-attachments/assets/3c214ada-d2c4-4a28-82a3-71568d403100" width="700">
   
 * Executed Multi-Branch Pipeline on Jenkins



<img src="https://user-images.githubusercontent.com/96679708/232276547-f007266b-677f-4ec5-a665-00375c8abfd4.png" width="700">

* as we can see the container is running 



<img src="https://user-images.githubusercontent.com/96679708/232275690-4a390cd7-0d85-4888-8711-f3482a415744.png" width="700">

*  Access Application on port 8080 in the browser



