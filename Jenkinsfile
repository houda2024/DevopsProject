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
                    echo 'Initializing global variables or performing setup...'

                    // Initialize global variables or perform any setup
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    docker.build("${IMAGE_NAME}:${TAG}")
                }
            }
        }

        stage('Testing') {
            steps {
                script {
                    echo 'Performing unit or integration tests...'
                    // Perform unit or integration tests
                    // Add your testing commands or scripts here
                }
            }
        }

        stage('Push to DockerHub') {
            steps {
                script {
                    // Push the built image to DockerHub
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub-credentials-id') {
                        docker.image("${IMAGE_NAME}:${TAG}").push()
                    }
                }
            }
        }

        stage('Cleanup') {
            steps {
                script {
                    echo 'Cleaning up resources or performing cleanup steps...'

                    // Clean up resources or perform any cleanup steps
                }
            }
        }
    }
}
