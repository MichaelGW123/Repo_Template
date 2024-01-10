pipeline {
    agent any

    environment {
        // Define environment variables here
        // EXAMPLE_PATH = '/path/to/example'
    }

    stages {
        stage('Checkout') {
            steps {
                // Get code from a source code repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Add commands to build your project
                // e.g., sh 'make build' or sh './build.sh'
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                // Add commands to test your project
                // e.g., sh 'make test' or sh './test.sh'
                echo 'Testing...'
            }
            post {
                always {
                    // Collect test results or perform cleanup
                    echo 'Collecting test results...'
                }
            }
        }

        stage('Deploy') {
            when {
                branch 'main' // or any branch condition or other condition
            }
            steps {
                // Add commands to deploy your project
                // e.g., sh './deploy.sh'
                echo 'Deploying...'
            }
        }
    }

    post {
        always {
            // Actions to perform after pipeline completion
            echo 'Pipeline completed.'
        }
        success {
            // Actions to perform if pipeline is successful
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform if pipeline fails
            echo 'Pipeline failed.'
        }
    }
}
