pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/your-username/simple-project.git'
            }
        }
        stage('Build Docker image') {
            steps {
                script {
                    dockerImage = docker.build("simple-project")
                }
            }
        }
        stage('Run Docker container') {
            steps {
                script {
                    dockerImage.run("-p 5000:5000")
                }
            }
        }
    }
}
