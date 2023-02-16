pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ -o cs104 cs104.cpp'
     
        echo "BUILD successful"
      }
    }
    stage('Test') {
      steps {
        sh './cs104'
        echo "TEST successful"
      }
    }
    stage('Deploy') {
      steps {
     
        echo "DEPLOY successful"
      }
    }
  }

  post {
    failure {
     echo 'Pipeline failed.'
    }
  }
}
