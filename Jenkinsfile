pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/aditya-sadavare/jenkinpython.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the project..."'
            }
        }
        stage('Test') {
            steps {
                sh 'python -m unittest discover -s ./ -p "test_*.py"'
            }
        }
    }
}