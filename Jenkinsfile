pipeline {
    agent any

    stages {

        stage('Welcome') {
            steps {
                echo 'Hello Sneha! Welcome to Jenkins.'
            }
        }

        stage('List Files') {
            steps {
                bat 'dir'
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

        stage('Run Docker Container') {
            steps {
                bat 'docker rm -f coffee-shop-container || exit 0'
                bat 'docker run -d -p 8081:80 --name coffee-shop-container coffee-shop:v1'
            }
        }

        stage('Check Running Containers') {
            steps {
                bat 'docker ps'
            }
        }

    }
}