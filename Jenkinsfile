pipeline {
    agent any
    environment {
        COMPOSE_DOCKER_CLI_BUILD = '1'  // Optional: speeds up builds with BuildKit
    }
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Hardik2102/two-tier-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker-compose build'  // or 'docker compose build' if using new CLI
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
