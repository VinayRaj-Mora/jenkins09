pipeline {
    agent {
        node{
            label 'AGENT-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    post{
        always {
            echo 'I will say hello always'
            cleanWs()
        }
        sucess {
            echo 'I will say hello sucess'
        }
        failure {
            echo 'I will say hello failuree'
        }
    }
}