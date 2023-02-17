pipeline {
    agent any
    stages {
      stage('Build') {
          steps {
              sh 'g++ -o myProgram PES1UG20CS134.cpp'
              build job: 'PES1UG20CS134-1'
              //build job: 'PES1UG20CS134-1 :) mistake'
          }
      }
      stage('Test') {
          steps {
              sh './myProgram'
          }
      }
      stage('Deploy') {
          steps {
              echo 'deployment successful'
          }
      }
  }

  post {
      failure {
          echo 'Pipeline failed'
      }
  }
}
