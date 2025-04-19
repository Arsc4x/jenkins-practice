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
                sh '''
                    python3 -m venv .venv
                    .venv/bin/pip3 install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                sh '.venv/bin/python3 -m pytest'
            }
        }
    }
}
