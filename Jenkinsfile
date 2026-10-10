pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        echo 'jenkins has checked out the repository'
      }
    }

    stage('Build') {
      steps {
        sh 'echo "Updated the jenkinsfile" '
        sh 'ls -la'
      }
    }

    stage('Test') {
      steps {
        sh 'echo " running tests" '
        sh 'test -f Jenkinsfile'
      }
    }
  }

  post {
    success {
      echo 'Succesfull '
    }
    failure {
      echo 'Build Failed '
    }
  }
}
