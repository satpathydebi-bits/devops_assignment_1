pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/satpathydebi-bits/devops_assignment_1.git'
            }
        }

        stage('Build and Compile') {
            steps {
                sh 'make build' 
                sh 'make compile' 
            }
        }
    }

    post {
        success {
            echo 'Build successful! Deploying...'
            // Add deployment steps if needed
        }
        failure {
            echo 'Build failed! Sending notification...'
            // Add notification steps if needed
        }
    }
}
