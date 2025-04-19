pipeline {
    agent {
        docker { image 'python:3.13-slim' }
    }
    stages {
        stage('Checkout') {
            steps {
                git url:'https://github.com/Arsc4x/jenkins-practice.git', branch: 'master'
            }
        }
        stage('Install') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest'
            }
        }
    }
}
