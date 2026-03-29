pipeline {
  agent none

  stages {
    stage('Test') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'node --version'
      }
    }

    stage('Run') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh "echo 'hi, i am dharanesh'"
      }
    }

    stage('Python') {
      agent {
        docker { image 'python:3.11-alpine' }
      }
      steps {
        sh 'python -c "print(\"helloworld\")"'
      }
    }
  }
}
