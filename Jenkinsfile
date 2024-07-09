pipeline {
    agent any

    environment {
        GIT_CREDENTIALS = 'github-token' // Replace with your GitHub credentials ID
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/venkatsatish07/Bangalore_North0786', credentialsId: env.GIT_CREDENTIALS
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add build steps here (e.g., Maven, Gradle, npm, etc.)
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add test steps here (e.g., unit tests, integration tests)
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment steps here (e.g., Docker, Kubernetes, SCP)
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
