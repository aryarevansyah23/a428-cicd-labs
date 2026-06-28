pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                    docker run --rm \
                      -v "$WORKSPACE":/app \
                      -w /app \
                      node:18-buster-slim \
                      npm install
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    docker run --rm \
                      -v "$WORKSPACE":/app \
                      -w /app \
                      -e CI=true \
                      node:18-buster-slim \
                      sh ./jenkins/scripts/test.sh
                '''
            }
        }
    }
}