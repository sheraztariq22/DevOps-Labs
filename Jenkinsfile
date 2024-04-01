pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git 'https://your-repository-url.git'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm run test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'npm start'
            }
        }
    }
}
