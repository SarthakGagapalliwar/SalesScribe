pipeline {
    agent any

    environment {
        APP_NAME = 'SalesScribe'
        DOCKER_IMAGE = 'salescribe:latest'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/SarthakGagapalliwar/SalesScribe.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m venv venv'
                sh './venv/bin/pip install --upgrade pip'
                sh './venv/bin/pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Add your test commands here
                echo 'No tests defined yet.'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8501:8501 $DOCKER_IMAGE'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
