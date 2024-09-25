pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'Devops-Pipeline' // Example image name
        GIT_URL = 'https://github.com/parvathy098/Devops-Pipeline.git' // Your repository URL
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // For Windows, use 'sh' instead of 'sh'
                sh 'echo Building the project on Windows'
                // Example for npm build or Docker build if you're using Node.js or Docker:
                // sh 'npm install'
                // sh 'docker build -t %DOCKER_IMAGE% .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Use 'sh' to run tests on Windows
                sh 'echo Running tests on Windows'
                // Example for Node.js testing:
                // sh 'npm test'
            }
        }

        stage('Code Quality Analysis') {
            steps {
                echo 'Running Code Quality Analysis...'
                // Example SonarQube analysis for Windows:
                sh 'echo Running SonarQube analysis'
                // If using SonarQube or another tool, integrate here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // For Docker Compose or any other Windows-friendly deployment tool
                sh 'echo Deploying the application on Windows'
                // Example for Docker Compose:
                // sh 'docker-compose up -d'
            }
        }

        stage('Release') {
            steps {
                echo 'Releasing the application...'
                sh 'echo Releasing the application to production'
                // Integrate release management commands (e.g., AWS CodeDeploy, Octopus)
            }
        }

        stage('Monitoring & Alerting') {
            steps {
                echo 'Setting up Monitoring and Alerting...'
                sh 'echo Monitoring production environment on Windows'
                // Integrate monitoring tools like Datadog or New Relic here
            }
        }
    }

    post {
        always {
            echo 'Cleaning up workspace...'
            cleanWs()
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
