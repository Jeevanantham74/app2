pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Jeevanantham74/app2.git'    
            }
        }
        stage('install dependencies') {
            steps {
                // Ensure a space is present after bat
                bat 'pip install -r requirements.txt'
            }
        }
        stage('run unit tests') {
            steps {
                // Fixed the missing space after bat
                bat 'pytest test_app.py'
            }
        }
    }
    post {
        always {
            echo 'Pipeline execution complete.'
        }
    }
}
