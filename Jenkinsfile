pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                git branch:'main',url:'https://github.com/Jeevanantham74/app2.git'    
            }
        }
        stage('install dependencies'){
            steps{
                bat'pip install-r requirements.txt'
            }
        }
        stage('run unit tests'){
            steps{
                bat'pytest test_app.py'
            }
        }
    }
}