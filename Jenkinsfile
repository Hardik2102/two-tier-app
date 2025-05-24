pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Hardik2102/two-tier-app.git'

            }
        }
        stage('Build') {
            steps {
                sh 'docker-compose build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
