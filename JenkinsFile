pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/mrudula-hingmire/food_order_system.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Docker Build & Push') {
            steps {
                script {
                    echo 'Building Docker image...'
                    sh 'docker build -t mrudula/food_order_system .'
                    echo 'Pushing Docker image...'
                    sh 'docker push mrudula/food_order_system'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
