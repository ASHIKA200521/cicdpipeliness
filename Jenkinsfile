pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/ASHIKA200521/cicdpipeliness.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 3000:3000 my-app'
            }
        }

    }
}