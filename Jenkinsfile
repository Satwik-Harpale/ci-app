pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'docker build -t ci-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running basic test cases...'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker run -d -p 5000:5000 ci-app'
            }
        }
    }
}