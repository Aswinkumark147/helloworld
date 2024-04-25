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
                sh 'npm install' // Assuming npm is installed on the Jenkins agent
            }
        }
        stage('Deploy') { // New stage for deployment
            steps {
                // Option 1: Using SSH Script Execution Plugin (preferred)
                script {
                    def server = "10.62.8.70" // Replace with your Red Hat server IP
                    def username = "testuser" // Replace with your username on the server
                    def password = "Achu@8347" // Replace with your password (consider using SSH keys for better security)

                    def scriptToRun = """
                    // Replace this with your actual deployment script commands
                    sudo yum install -y  // Example command
                    cd /home/testuser@credopay.com/
                    npm run deploy  // Assuming you have a deploy script in your project
                    """

                    sh """
                    sshpass -p ${Achu@8347} ssh -o StrictHostKeyChecking=no ${testuser}@${10.62.8.70} "${home/testuser@credopay.com/deploy.sh}"
                    """
                }

            }
        }
    }
}
