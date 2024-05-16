pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Frontend Docker Image') {
            steps {
                dir('client') {
                    sh 'docker build -t my-frontend-app .'
                }
            }
        }

        stage('Build Backend Docker Image') {
            steps {
                dir('backend') {
                    sh 'docker build -t my-backend-app .'
                }
            }
        }
    }

    post {
        success {
            echo 'Builds completed successfully.'
        }

        failure {
            echo 'Builds failed.'
        }
    }
}
