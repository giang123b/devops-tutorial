pipeline {
   agent any
    stages{
        stage('Clone'){
            steps{
                git 'https://github.com/giang123b/devops-tutorial.git'
            }
        }
       stage('Build'){
            steps{
               withDockerRegistry(credentialsId: 'docker-hub3', url: 'https://index.docker.io/v1/') {
                  sh 'docker build -t giangdt3/test:v10.'
                  sh 'docker bpúh giangdt3/test:v10'
               }
            }
        }
    }
}
