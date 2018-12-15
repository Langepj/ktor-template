pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                sh 'chmod +x gradlew'
                sh './gradlew build'
            }
        }
        stage('Spin up Container'){

            steps{
                sh 'docker build -t app-template .'
                sh 'docker run --name template -d -p 8081:8081 --rm app-template:latest'
                sh 'docker stop template'
            }

        }

        stage('Test') {
            steps {
                sh 'echo No tests available'
            }
        }
    }


}