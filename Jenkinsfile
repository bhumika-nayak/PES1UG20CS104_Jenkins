pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ -o cs104 cs104.cpp'
        build job: 'PES1UG20CS104_BHUMIKA-1'
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
