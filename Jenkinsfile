pipeline {
    stages {
        stage("Build") {
            steps {
                echo "Building" && make
            }
        }
        stage("Test") {
            steps {
                echo "Testing" && ./hello_exec
            }
            post {
                failure {
                    echo "Test stage failed. Notifying developers..."
                }
            }
        }
    }
}
