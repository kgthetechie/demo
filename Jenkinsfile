pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building..."'
                // Add build steps here
            }
        }
        
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
                // Add test steps here
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
                // Add deployment steps here
            }
        }
    }
    
    post {
        always {
            sh 'echo "Pipeline finished"'
        }
    }
}