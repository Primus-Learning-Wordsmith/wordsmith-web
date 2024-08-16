pipeline {
    agent any

    tools{
        maven 'Apache Maven 3.9.8'
    }

    stages{
        stage('Build Docker Image') {
            steps{
                script{
                    sh 'docker build -t Primus-Learning-Wordsmith/wordsmith-web .'
                }
            }
        }
        
        stage('Push to Dockerhub') {
            steps{
                sh 'docker push Primus-Learning-Wordsmith/wordsmith-web'
            }
        }
    }
}