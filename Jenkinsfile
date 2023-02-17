pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS134 PES1UG20CS134.cpp'
                echo 'BUILD SUCCESSFUL'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS134'// correct
                //sh './PES' //incorrect
            }
        }

        stage('Deploy') {
            steps {
                echo 'DEPLOYMENT SUCCESSFUL'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
