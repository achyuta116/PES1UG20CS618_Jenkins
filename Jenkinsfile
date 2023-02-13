pipeline {
    stages {
        stage('Build') {
            steps {
                make
            }
        }
        stage('Test') {
            steps {
                build job: 'PES1UG20CS618-2'
            }
            post {
                failure {
                    echo 'Test stage failed. Notifying developers...'
                }
            }
        }
    }
}

