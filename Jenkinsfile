
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting the source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the HTML application'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                bat 'if exist index.html (echo HTML file found) else (exit 1)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'HTML application pipeline completed'
            }
        }
    }
}
