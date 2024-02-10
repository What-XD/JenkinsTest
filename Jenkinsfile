pipeline {
    agent any 
    stages {
        stage('Docker version') { 
            steps {
                sh 'docker version'
            }
        }
        stage('Delete') {
            steps {
                deleteDir()
            }
        }
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/What-XD/JenkinsTest.git'
            }
        }
        stage('Build docker compuse') {
            steps {
                sh 'docker-compose up --build -d'
            }
        }
    }
}