pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/vu2f2425004/prabhjot-devops-project.git' 
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t student-app .'
            }
        }
        stage('Deploy Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name student-container student-app'
            }
        }
    }
}