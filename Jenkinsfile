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
                sh 'python app.py'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'python -m pytest'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building application'
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
