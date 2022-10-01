pipeline {
    agent {
        kubernetes {
            namespace 'cicd'
            containerTemplate 'node:lts-bullseye-slim'
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
