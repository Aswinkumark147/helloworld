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
                npm install --save express
                npm install --save-dev supertest should mocha
                sudo npm install -g mocha
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
