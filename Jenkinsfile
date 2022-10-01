pipeline {
    agent {
        kubernetes {
            name 'node-build-agent'
            image 'node:lts-bullseye-slim'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'test', credentialsId: 'GitHubService', url: 'https://github.com/khastings256/off-the-tube-web.git'
            }
        }
        stage('Build') {
            steps {
                sh 'npm build'
            }
        }
    }
}
