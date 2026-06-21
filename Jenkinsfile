pipeline {
    agent {
        docker {
            image 'node:18-buster-slim'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}