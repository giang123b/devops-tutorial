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
               withDockerRegistry(credentialsId: 'docker-hub2') {
                  sh 'docker build -t giangdt3/devops-tutorial:v10.'
                  sh 'docker build giangdt3/devops-tutorial:v10'
               }
            }
        }
    }
}
