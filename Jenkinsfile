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
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'pytest'
            }
        }
    }
}
