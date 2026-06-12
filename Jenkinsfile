pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = 'Jenkins 09 - Declarative Pipeline'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building..."
                        echo $COURSE
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing..."
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying..."
                    """
                }
            }
        }
    }
    post {
        always {
            echo 'This will always run.'
            cleanWs()
        }
        success {
            echo 'This will run only if the build succeeds.'
        }
        failure {
            echo 'This will run only if the build fails.'
        }
    }
}