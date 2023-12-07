pipeline {
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'rm -rf node_modules'
                sh 'npm cache clean --force'
                sh 'npm install'
            }
        }
    }
}