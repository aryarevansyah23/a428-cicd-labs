pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
            sh '''
                docker run --rm \
                    -v "${WORKSPACE}:/app" \
                    -w /app \
                    node:18-buster-slim \
                    npm install
            '''
            }
        }
    }
}