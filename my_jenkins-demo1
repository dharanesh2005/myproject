pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
      }
    }
    stage('Run'){
      steps {
       sh "echo 'hi,i am dharanesh'"
      }
    }
  }
}
