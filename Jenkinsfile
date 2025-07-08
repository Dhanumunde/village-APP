pipeline {
  agent any

  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/Dhanumunde/village-APP.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t koyal-app .'
      }
    }

    stage('Run Container') {
      steps {
        sh 'docker run -d -p 3000:3000 koyal-app'
      }
    }
  }
}

