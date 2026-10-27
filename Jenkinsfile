
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                bat 'javac App.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java App'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline executed successfully!'
        }
        failure {
            echo 'CI Pipeline failed. Check Console Output.'
        }
    }
}
