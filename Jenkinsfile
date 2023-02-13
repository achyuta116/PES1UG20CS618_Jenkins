pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                make
            }
            post {
                failure {
                    echo 'Build stage failed'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                ./hello_exec
            }
            post {
                failure {
                    echo 'Test stage failed'
                }
            }
        }
    }
}
