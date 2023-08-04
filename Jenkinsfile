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
                sh 'cp -r /Users/hari/.jenkins/workspace/My_Pipeline_1/index.html /Applications/tomcat/webapps/ROOT/index.html'
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