pipeline {
    agent any
    tools {
        maven 'Maven-3.6.3' 
    }
    stages {
        stage('Build Project') {
            steps {
                echo "Building the Maven project via Jenkinsfile..."
                sh 'mvn clean install'
            }
        }
    }
}
