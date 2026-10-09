pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Verify Environment') {
            steps {
                bat 'python --version'
                bat 'python -m pytest --version'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python -m pytest -v'
            }
        }
    }

    post {
        success {
            echo 'All tests passed successfully!'
        }

        failure {
            echo 'Tests failed. Check the Console Output.'
        }

        always {
            echo 'Jenkins Continuous Testing Pipeline completed.'
        }
    }
}
