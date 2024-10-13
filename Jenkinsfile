pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup') {
            steps {
                sh 'python3 -m venv venv'
                sh '''
                   . venv/bin/activate
                   pip3 install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                   . venv/bin/activate 
                   python3 -m unittest discover tests
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
                // Add your deployment steps here
            }
        }
    }

    post {
        always {
            sh 'deactivate || true'
            sh 'rm -rf venv'
        }
    }
}
