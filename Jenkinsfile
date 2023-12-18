pipeline {
    agent any

    environment {
        // Global variables
        IMAGE_NAME = 'houda2024/devpopsprojectmicro'
        TAG = 'latest'
        DOCKERHUB_CREDENTIALS_ID = '6703e9d2-1dc9-4b4d-8e49-58571d98b4f1'
        REGISTRY_URL = 'https://registry.hub.docker.com'
    }

    stages {
        stage('Initialization') {
            steps {
                script {
                    echo '=== Initialization ==='
                    // Initialize global variables or perform any setup
                    // You may add additional setup steps here
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    echo '=== Build ==='
                    // Build Docker image
                    docker.build('houda2024/devpopsprojectmicro')
                }
            }
        }

        stage('Testing') {
            steps {
                script {
                    echo '=== Testing ==='
                    sh 'npm test'
                    // Perform unit or integration tests
                    // Add your testing commands or scripts here
                }
            }
        }

        stage('Push to DockerHub') {
            steps {
                script {
                    echo '=== Push to DockerHub ==='
                    // Push the built image to DockerHub
                    docker.withRegistry(REGISTRY_URL, DOCKERHUB_CREDENTIALS_ID) {
                        docker.image('houda2024/devpopsprojectmicro').push()
                    }
                }
            }
        }

        stage('Cleanup') {
            steps {
                script {
                    echo '=== Cleanup ==='
                    // Clean up resources or perform any cleanup steps
                    // You may add additional cleanup steps here
                }
            }
        }
    }
}
