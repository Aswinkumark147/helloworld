pipeline {
    agent any 
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
                
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'chmod +x /home/aswinkumark147/deploy.sh'
                sh '/home/aswinkumark147/deploy.sh'
            }
        }
    }
}
