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
                npm i --save express
                npm i --save-dev supertest should mocha
                sudo npm i -g mocha
            }
        }
                
        stage('Test') {
            steps {
                npm test
                npx serve
            }
        }
    }
}
