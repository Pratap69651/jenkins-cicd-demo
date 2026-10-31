pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Source code checkout completed'
                sh 'ls -la'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running application tests'
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
                sh 'echo Application deployed successfully'
            }
        }
    }

    post {
        success {
            echo 'CI/CD pipeline completed successfully'
        }

        failure {
            echo 'CI/CD pipeline failed'
        }

        always {
            echo 'Pipeline execution finished'
        }
    }
}
