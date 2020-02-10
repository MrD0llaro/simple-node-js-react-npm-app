pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000 --dns=10.122.1.184' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install debug' 
            }
        }
    }
}