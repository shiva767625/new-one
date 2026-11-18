pipeline {
    agent any
    
    tools {
        maven 'Maven-3.6.3' 
    }
    
    stages {
        stage('Download Application Code') {
            steps {
                echo "Downloading the Amazon project code from GitHub..."
                dir('amazon-code') {
                    git branch: 'main', url: 'https://github.com/PraveenKuberABC/Amazon-Jenkins'
                }
            }
        }
        
        stage('Build Project') {
            steps {
                echo "Building the Maven project..."
                dir('amazon-code') {
                    sh 'mvn clean install'
                }
            }
        }
    }
    
    post {
        success {
            echo "✅ SUCCESS: The Jenkinsfile executed perfectly!"
        }
        failure {
            echo "❌ FAILURE: The pipeline encountered an error."
        }
    }
}
