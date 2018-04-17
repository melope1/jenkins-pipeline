pipeline {
  agent {
    docker {
      image 'golang:1.10.1-alpine'
    }
    
  }
  stages {
    stage('say hello') {
      steps {
        echo "Hello ${MY_NAME}"
        sh 'go version'
      }
    }
  }
  environment {
    MY_NAME = 'Mario'
  }
}