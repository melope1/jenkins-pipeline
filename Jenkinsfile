library 'SharedLibs'
pipeline {
  agent any
  stages {
    stage('say hello') {
      steps {
        echo "Hello ${params.Name}"
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
    stage('Shared Lib') {
      steps {
        helloWorld("Jenkins")
      }
    }
  }
  environment {
    TEST_USER = credentials('test-user')
  }
  post {
    aborted {
      echo 'Why didn\'t you push my button?'
      
    }
    
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}
