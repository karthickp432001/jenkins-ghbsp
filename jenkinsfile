pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Replace this with your actual build command
                sh 'echo "Build step executed"'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Replace this with your actual test command
                sh 'echo "Test step executed"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
