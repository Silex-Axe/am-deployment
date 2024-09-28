pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Clone the centralized deployment repository
                git branch: 'main', url: 'https://github.com/Silex-Axe/am-deployment.git'
            }
        }

        stage('Load Jenkinsfile') {
            steps {
                // Load Jenkinsfile specific to service
                load 'ci-cd/Jenkinsfile-auth'
            }
        }
    }
}