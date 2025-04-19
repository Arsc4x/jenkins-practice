pipeline {
    agent any
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
