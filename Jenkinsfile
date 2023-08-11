pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the repository
                checkout scm
            }
        }
        
        stage('Build and Test') {
            steps {
                // Run Maven clean and test goals
                echo 'mvn clean test'
            }
        }
    }
    
    post {
        success {
            echo 'Build and tests were successful!'
            // Add additional steps for deployment or notifications if needed
        }
        failure {
            echo 'Build or tests failed!'
            // Add additional steps for notifications or cleanup if needed
        }
    }
}
