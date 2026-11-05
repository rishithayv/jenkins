
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Application') {
            steps {
                bat 'python app.py'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python -m pytest'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Building application'
            }
        }
    }

    post {
        success {
            echo 'Jenkins Build Successful'
        }
        failure {
            echo 'Jenkins Build Failed'
        }
    }
}
