pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout stage running'
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Build stage running'
                sh 'docker-compose build'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Test stage running'
                // Add your tests here
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy stage running'
                sh 'docker-compose up -d'
            }
        }
        
        stage('Integration Test') {
            steps {
                echo 'Integration Test stage running'
                // Add integration tests here
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed'
        }
    }
}