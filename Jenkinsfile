pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-demo:latest .'
            }
        }

        stage('Test Image') {
            steps {
                sh 'docker images | grep jenkins-demo'
            }
        }

        stage('Run container') {
            steps {
                sh '''
                docker rm -f demo-app || true
                docker run -d --name demo-app -p 5000:5000 jenkins-demo:latest
                '''
            }
        }
    }
}
