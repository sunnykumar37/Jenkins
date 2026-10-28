
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting code from GitHub'
                checkout scm
            }
        }

        stage('Test HTML') {
            steps {
                bat 'if exist index.html (echo HTML file found) else (exit 1)'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t student-app:v1 .'
            }
        }

        stage('Verify Docker Image') {
            steps {
                bat 'docker images student-app'
            }
        }
    }
}
