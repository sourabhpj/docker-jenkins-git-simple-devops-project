pipeline {
   agent any

stages {

    stage('Clone Code') {
        steps {
            git 'https://github.com/sourabhpj/docker-jenkins-git-simple-devops-project.git'
        }
    }

    stage('Build Docker Image') {
        steps {
            sh 'docker build -t my-website .'
        }
    }

    stage('Run Container') {
        steps {
            
                 sh  'docker stop my-container || true'
                  sh 'docker rm my-container || true'
                   sh 'docker run -d -p 80:80 --name my-container my-website'
            
        }

        }
    }
}