pipeline {
    agent any

    tools {
        nodejs 'NodeJS-20'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ragulm456/nodejs-jenkins-cicd.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Node.js application...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t nodejs-demo-app:latest .'

                echo 'Stopping old container if it exists...'
                sh 'docker rm -f nodejs-demo-container || true'

                echo 'Starting new container...'
                sh 'docker run -d --name nodejs-demo-container -p 3000:3000 nodejs-demo-app:latest'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}