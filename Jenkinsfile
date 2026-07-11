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
                sh 'docker build -t githubtest:v1 .'
            }
        }

        stage('Remove Old Container') {
            steps {
                sh 'docker rm -f githubtest-container || true'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d --name githubtest-container -p 8081:80 githubtest:v1'
            }
        }

        stage('Verify Container') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
