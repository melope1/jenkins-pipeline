pipeline {
  agent {
    docker {
      image 'golang:1.10.1-alpine'
      label 'docker-cloud'
    }
    
  }
  stages {
    stage('say hello') {
      steps {
        echo 'Hello, world!'
        sh 'go version'
      }
    }
  }
}