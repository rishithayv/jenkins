pipeline {
    agent any
    triggers { githubPush() }

    stages {
        stage('Checkout') {
            steps { checkout scm }
        }
        stage('Build') {
            steps {
                sh 'javac -version'
                sh 'javac App.java AppTest.java'
            }
        }
        stage('Test') {
            steps { sh 'java AppTest' }
        }
    }

    post {
        success { echo 'Build stable' }
        failure { echo 'Build failed' }
    }
}
