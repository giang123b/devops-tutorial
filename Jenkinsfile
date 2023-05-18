pipeline {
   agent any
    stages{
        stage('Clone'){
            steps{
                git 'https://github.com/giang123b/devops-tutorial.git'
            }
        }
       stage('Build image') {
           app = docker.build("giangdt/demodevops")
       }
    }
}
