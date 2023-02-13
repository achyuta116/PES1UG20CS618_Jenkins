pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build job: 'PES1UG20CS618-1' 
            }
        }
        stage('Test') {
            steps {
                build job: 'PES1UG20CS618-2'
            }
            post {
                failure {
                    echo 'pipeline failed: testing stage'
                }
            }
        }
    }
}

