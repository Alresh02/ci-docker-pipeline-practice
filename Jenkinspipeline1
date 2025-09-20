pipeline {
  agent any

  environment {
    IMAGE_NAME = 'ci-docker-image:latest'
  }

  stages {
    stage('Checkout Code') {
      steps {
        git branch: 'main', url: 'https://github.com/Alresh02/ci-docker-pipeline-practice.git'
      }
    }
    stage('Build Docker Image') {
      steps {
        bat "docker build -t %IMAGE_NAME% ."
      }
    }

    stage('Show Docker Images') {
      steps {
        bat "docker images"
      }
    }
  }
}
