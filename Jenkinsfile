pipeline {
    agent any

    environment {
        IMAGE_NAME = 'python-flask-app'
        CONTAINER_NAME = 'python-flask-container'
    }

    stages {
        
        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                bat 'docker build -t %IMAGE_NAME% .'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Installing dependencies & running tests...'
                bat 'pip install -r requirements.txt'
                bat 'pytest test_app.py'
            }
        }

        stage('Deploy Container') {
            steps {
                echo 'Deploying Docker container...'
                bat '''
                    docker stop %CONTAINER_NAME% || echo Container not running
                    docker rm %CONTAINER_NAME% || echo Container not found
                    docker run -d --name %CONTAINER_NAME% -p 5000:5000 %IMAGE_NAME%
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
