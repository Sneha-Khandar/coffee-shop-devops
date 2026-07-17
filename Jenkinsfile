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
    }
}