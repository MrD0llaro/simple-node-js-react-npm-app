pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000 --dns=10.122.1.184' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install debug' 
            }
        }
        stage('Test') {
            steps {
                sh 'npm i -g react-scripts'
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}