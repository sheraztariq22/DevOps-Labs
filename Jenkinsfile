pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/sheraztariq22/DevOps-Labs.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t express-mongodb-app:latest .'
            }
        }

        stage('Test') {
            steps {
                echo "No tests found in package.json. Skipping test stage."
            }
        }

        stage('Start Docker Compose Services') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }

    post {
        always {
            sh 'docker-compose down'
        }
    }
}
