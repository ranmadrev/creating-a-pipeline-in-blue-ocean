pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      agent {
        docker {
          image 'node:6-alpine'
          args '-p 3000:3000'
        }

      }
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh 'sh /root/GITHUB/creating-a-pipeline-in-blue-ocean/jenkins/scripts/test.sh'
      }
    }
  }
  environment {
    CI = 'true'
  }
}