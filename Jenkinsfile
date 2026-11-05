
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
                bat '"C:\\Users\\STUDENT\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
            }
        }

        stage('Run Tests') {
            steps {
                bat '"C:\\Users\\STUDENT\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pytest'
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
