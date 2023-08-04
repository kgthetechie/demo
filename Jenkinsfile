pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {

                checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/kgthetechie/demo.git']]])
            }
        }
        
        stage('Build') {
            steps {
                // Assuming you need to build your web application, put the build commands here
                // For example: sh 'npm install' or 'mvn package' or any build commands specific to your project
                sh 'echo "Building..."'
            }
        }

        stage('Deploy to Web Server') {
            steps {
                // Copy the built files to the web server directory (e.g., Apache's DocumentRoot)
                // Replace '/path/to/apache/web/root' with the actual path of your Apache DocumentRoot
                sh 'cp -r /Users/hari/.jenkins/workspace/My_Pipeline_1/* /Applications/tomcat/webapps/ROOT/'


                // Optionally, you can restart the Apache server after deploying
                // Make sure Jenkins has sufficient permissions to restart the Apache server
                
                sh '/Applications/tomcat/bin/catalina.sh stop'
                sh '/Applications/tomcat/bin/catalina.sh start'
            }
        }
        stage('Verify') {
            steps {
                sh 'echo "Pipeline finished"'
            }
        }
     }
}
