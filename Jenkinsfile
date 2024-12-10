pipeline {
    agent any
    
    Stages {
        Stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine

                }echo 'Hello World'
            }
        }
    }
}

pipeline {
    agent any
    stages {  // Use lowercase 'stages'
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true 
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run Build
                    ls -la
                '''