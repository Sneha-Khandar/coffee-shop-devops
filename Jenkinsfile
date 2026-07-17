pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                echo 'Code downloaded successfully.'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t coffee-shop:v1 .'
            }
        }

        stage('Docker Images') {
            steps {
                bat 'docker images'
            }
        }
    }
}