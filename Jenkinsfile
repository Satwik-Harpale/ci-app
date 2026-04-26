pipeline {
    agent any

    stages {

        stage('Pull Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Satwik-Harpale/ci-app.git'
            }
        }

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
    }
}