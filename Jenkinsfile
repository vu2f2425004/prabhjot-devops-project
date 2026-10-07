pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/vu2f2425004/prabhjot-devops-project.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t student-app .'
            }
        }
        stage('Deploy Container') {
            steps {
                bat 'docker run -d -p 5000:5000 --name student-container student-app'
            }
        }
    }
}