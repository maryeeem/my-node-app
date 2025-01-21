pipeline {
    agent any
    tools { 
        nodejs "NodeJS 23.6.0" // Use the name you gave in Global Tool Configuration
    }
    stages {
        stage('Build') {
            steps {
                sh 'node -v'
                sh 'npm install'
                sh 'npm start'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
    
}
