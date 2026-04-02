pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "devops-app"
        DOCKER_TAG = "latest"
    }

    stages {

        stage('Clone Code') {
            steps {
                echo "Cloning repository..."
                git 'https://github.com/koppulasharath/devops-cicd-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "Building Docker image..."
                sh 'docker build -t $DOCKER_IMAGE:$DOCKER_TAG .'
            }
        }

        stage('Run Container') {
            steps {
                echo "Running Docker container..."
                sh '''
                docker stop devops-container || true
                docker rm devops-container || true
                docker run -d -p 3000:3000 --name devops-container $DOCKER_IMAGE:$DOCKER_TAG
                '''
            }
        }

        stage('Verify') {
            steps {
                echo "Checking running containers..."
                sh 'docker ps'
            }
        }
    }
