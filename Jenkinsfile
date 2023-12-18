pipeline {
    agent any

    environment {
        // Global variables
        IMAGE_NAME = 'houda2024/devpopsprojectmicro'
        TAG = 'latest'
        REGISTRY_URL = 'https://index.docker.io/v1/'
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
                    // Push the built image to DockerHub without explicit credentials
                    
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
