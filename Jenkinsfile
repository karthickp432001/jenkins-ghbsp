pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code...'
                checkout scm
            }
        }

        stage('Conditional Stages') {
            when {
                expression {
                    return env.BRANCH_NAME == 'dev' || env.CHANGE_ID != null
                }
            }
            stages {
                stage('Build') {
                    steps {
                        echo 'Building the project...'
                        sh 'echo "Build step executed"'
                    }
                }
                stage('Test') {
                    steps {
                        echo 'Running tests...'
                        sh 'echo "Test step executed"'
                    }
                }
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
