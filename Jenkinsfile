pipeline {
    agent {
        kubernetes {
            image 'node:lts-bullseye-slim'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm build'
            }
        }
    }
}
