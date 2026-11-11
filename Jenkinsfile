pipeline {
    agent any

    stages {
        stage('Checkout from GitHub') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Muhannadkhan/devops-cicd-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-devops-app .'
            }
        }

        stage('Deploy Application') {
            steps {
                sh 'docker stop my-devops-container || true'
                sh 'docker rm my-devops-container || true'
                sh 'docker run -d --name my-devops-container -p 8080:80 my-devops-app'
            }
        }
    }
}
