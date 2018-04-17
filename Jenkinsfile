pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('say hello') {
      steps {
        echo 'Hello, world!'
        sh 'java -version'
      }
    }
  }
}