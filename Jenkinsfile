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
                npm test
                npx serve
            }
        }
        stage('Deploy') {
            steps {
                sh 'home/aswinkumark147/deploy.sh'
            }
        }
    }
}
