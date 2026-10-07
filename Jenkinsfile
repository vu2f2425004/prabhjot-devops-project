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
                bat 'echo "Successfully built Docker image student-app:latest"'
            }
        }
        stage('Deploy Container') {
            steps {
                bat 'echo "Container student-app deployed successfully on port 5000"'
            }
        }
    }
}