pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/aditya-sadavare/jenkinpython.git'
            }
        }
        stage('Build') {
            steps {
                bat 'echo "Building the project..."'
            }
        }
        stage('Test') {
            steps {
                bat '"C:\\Users\\adity\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" -m unittest discover -s ./ -p "test.py"'
            }
        }
    }

    post {
        success {
            emailext(
                subject: "Pipeline SUCCESS: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "The pipeline ${env.JOB_NAME} succeeded. Build #${env.BUILD_NUMBER}.",
                to: 'recipient_email@example.com'
            )
        }
        failure {
            emailext(
                subject: "Pipeline FAILURE: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "The pipeline ${env.JOB_NAME} failed. Build #${env.BUILD_NUMBER}.",
                to: 'recipient_email@example.com'
            )
        }
    }
}
