pipeline {
    agent any

    tools{
        maven 'Apache Maven 3.9.8'
    }

    stages{
        stage('Build Docker Image') {
            steps{
                script{
                    sh 'docker build -t grace414/wordsmith_web:latest .'
                }
            }
        }
        
        stage('Push to Dockerhub') {
            steps{
                sh 'docker push grace414/wordsmith_web:latest'
            }
        }
    }
}