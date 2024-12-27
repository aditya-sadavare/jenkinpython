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
                bat 'python -m unittest discover -s ./ -p "test_*.py"'
            }
        }
    }
}
