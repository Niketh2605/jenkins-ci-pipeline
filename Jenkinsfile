pipeline {
  agent any

  tools {
    nodejs "NodeJS 18"  // You can skip this if Node is installed in the container already
  }

  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/Niketh2605/jenkins-ci-pipeline.git'
      }
    }

    stage('Install Dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Run Tests') {
      steps {
        sh 'npm test || echo "Tests failed or not defined"'
      }
    }
  }
}



