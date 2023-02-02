pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:lts-bullseye-slim'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'node -v'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

  }
}