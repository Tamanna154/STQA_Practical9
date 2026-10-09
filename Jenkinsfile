pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                bat 'git status'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python -m pytest'
            }
        }
    }
}