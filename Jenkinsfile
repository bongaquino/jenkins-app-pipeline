pipeline {
    agent any

    tools {
        nodejs "NodeJS" // This refers to the NodeJS installation in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/bongaquino/jenkins-app-pipeline.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deployment steps here
            }
        }
    }
}
