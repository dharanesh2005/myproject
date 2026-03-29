pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Test') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'node --version'
      }
    }
    stage('Run'){
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
       sh "echo 'hi,i am dharanesh'"
      }
    }
    stage('java'){
      agent {
        docker { image 'python:3.11-alpine' }
      }
      step {
        sh " print('helloworld')"
      }
    }
    stage('DB'){
      agent {
        docker { 
          image 'mysql:8'
          args '-e MYSQL_ROOT_PASSWORD=root'
        }
      }
      step{
        sh " mysql -u root -proot -e "SHOW DATABASES;" "
      }
    }
  }
}
