#!/usr/bin/env groovy

// CD - Deploy Application from Jenkins Pipeline to EC2 Instance (automatically with docker)


library identifier: 'jenkins-shared-library@master', retriever: modernSCM(
        [$class: 'GitSCMSource',
         remote: 'https://gitlab.com/Rajib-Mardi/jenkins-shared-library.git',
         credentialsId: 'gitlab-token'
        ]
)



pipeline {
    agent any
    tools {
        maven 'maven-3.9'
    }
    environment {
        IMAGE_NAME = 'rajibmardi/my-repo:java-maven-1.0'
    }
    stages {

        stage("build app") {
            steps {
                script {
                    echo 'building application jar...'
                    buildJar()
                }
            }
        }
        stage("build and push image") {
            steps {
                script {
                    echo 'building docker image...'
                    buildImage(env.IMAGE_NAME)
                    dockerLogin()
                    dockerPush (env.IMAGE_NAME)
                }
            }
        }

        stage('deploy') {
            steps {
                script {
                    echo 'deploying docker image to EC2'
                    def dockerCmd = "docker run -p 8080:8080 -d ${IMAGE_NAME}"
                    sshagent(['ec2-server-key']) {
                        sh "ssh -o StrictHostKeyChecking=no ec2-user@18.142.228.154 ${dockerCmd}"
                    }
                }   
             }
        }
    }
}  

