pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  environment {
    DOCKERHUB_CREDENTIALS = credentials('docker-hub')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t giangdt3/usecase1 .'
      }
    }
    stage('Login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }
    stage('Push') {
      steps {
        sh 'docker push giangdt3/demodevops'
      }
    }
  }
//   post {
//     always {
//       sh 'docker logout'
//     }
//   }
}
