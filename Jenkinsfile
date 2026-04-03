pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/bujji3619/Automated-CI-CD-Pipeline-for-a-2-Tier-Flask-Application-on-AWS.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building Flask App...'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t flask-app .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 80:5000 flask-app'
            }
        }
    }
}
