pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Checkout your git repo
                git branch: 'main', url: 'https://github.com/Hardik2102/two-tier-app.git'
            }
        }
        stage('Build') {
            steps {
                // Build images with docker-compose
                sh 'docker-compose build'
            }
        }
        stage('Deploy') {
            steps {
                // Run containers detached mode
                sh 'docker-compose up -d'
            }
        }
    }
}
