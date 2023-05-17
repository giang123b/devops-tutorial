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
               withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
                  
                  sh 'docker push giangdt3/demodevops'
               }
            }
        }
    }
}
