pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
    stage('PreBuild') { 
            steps {
                sh 'npm init' 
            }
        },
        stage('Build') { 
            steps {
                sh 'npm install debug' 
            }
        }
    }
}