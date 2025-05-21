pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the application..."'
                sh 'docker build -t my-python-app .'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                // Ajoute ici tes tests si besoin
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying locally..."'
                sh 'docker stop my-python-app || true'
                sh 'docker rm my-python-app || true'
                sh 'docker run -d -p 5000:5000 --name my-python-app my-python-app'
            }
        }
    }
}
