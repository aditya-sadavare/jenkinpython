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
                bat '"C:\\Users\\adity\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" -m unittest discover -s ./ -p "test_main.py"'
            }
        }
    }
}
