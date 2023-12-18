pipeline {
    agent any

    environment {
        // Global variables
        IMAGE_NAME = 'houda2024/devpopsprojectmicro'
        TAG = 'latest'
        
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
                    docker.build("${IMAGE_NAME}:${TAG}")
                }
            }
        }

        stage('Testing') {
            steps {
                script {
                    echo '=== Testing ==='
                    
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
                        docker.image("${IMAGE_NAME}:${TAG}").push()
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
