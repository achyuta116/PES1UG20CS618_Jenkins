pipeline {
    stages {
        stage('Build') {
            steps {
                make
            }
        }
        stage('Test') {
            steps {
                ./hello_exec
            }
            post {
                failure {
                    echo 'Test stage failed. Notifying developers...'
                }
            }
        }
    }
}

