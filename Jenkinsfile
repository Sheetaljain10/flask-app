pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Sheetaljain10/flask-app.git'
            }
        }
        stage('Setup Python Environment') {
            steps {
                sh '''
                python -m venv venv
                source venv/bin/activate
                pip install -r requirements.txt
                '''
            }
        }
        stage('Run Flask App') {
            steps {
                sh '''
                python app.py &
                '''
            }
        }
    }
}
