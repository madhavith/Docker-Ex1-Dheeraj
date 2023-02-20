pipeline {
    agent any
    environment{
        DOCKER_IMAGE_NAME = "sample-doc-img"
        DOCKER_IMAGE_VERSION = "1.0.0"
        DOCKER_REGISTRY_URL = "docker.io"
        DOCKER_REGISTRY_CREDENTIALS_ID = "dockerpasswd"
    }
    stages {        
        stage('Git Checkout') {          
            steps {                
                git 'https://github.com/madhavith/Docker-Ex1-Dheeraj.git'            
                }        
        }
        stage('Image Build') {
            steps {
                script {
                    docker.build("${DOCKER_REGISTRY_URL}/${DOCKER_IMAGE_NAME}:${DOCKER_IMAGE_VERSION}", '-f Dockerfile .')
                }
            }
        }
        
    }
}

