pipeline {
    agent any

    stages {
        stage('GitHub Pipeline') {
            steps {
                echo 'Hello John from GitHub Jenkinsfile'
            }
        }

        stage('Show Files') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }
    }
}
