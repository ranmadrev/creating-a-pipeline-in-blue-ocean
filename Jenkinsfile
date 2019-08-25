pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh 'GITHUB/creating-a-pipeline-in-blue-ocean/jenkins/scripts/test.sh'
      }
    }
  }
}