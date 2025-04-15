pipeline {
    agent any
    stages {
        stage('version') {
            steps {
                sh 'python --version'
            }
        }
        stage('Build') {
            steps {
                sh 'python dummyvers.py'
            }
        }
    }
}
