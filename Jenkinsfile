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
        stage('Lint') {
            steps {
                sh 'npm run lint'
            }
        }
        stage('Security Scan') {
            steps {
                sh 'npm audit'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
            post {
                always {
                    junit 'test-results.xml'
                }
            }
        }
    }
}
