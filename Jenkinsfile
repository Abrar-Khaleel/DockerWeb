pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git https://github.com/Abrar-Khaleel/DockerWeb.git
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t web-image-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8090:80 web-image-app'
            }
        }
    }
}