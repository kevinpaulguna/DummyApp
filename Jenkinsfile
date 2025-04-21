pipeline {
    agent any

    environment {
        VENV = 'venv'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/kevinpaulguna/DummyApp.git'  // or use a GitHub repo you have
            }
        }

        stage('Setup Python') {
            steps {
                sh 'python -m venv $VENV'
                sh './$VENV/bin/pip install --upgrade pip'
                sh './$VENV/bin/pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh './venv/bin/python -m unittest discover -s tests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step — this can be uploading to server, Docker, etc.'
            }
        }
    }
}
