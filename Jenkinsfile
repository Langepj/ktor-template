pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                sh './gradlew build'
            }
        }
        stage('Spin up Container'){
            agent { dockerfile{
                additionalBuildArgs '-p 8081:8081'
            } }
            steps{
                sh 'echo Spinning up Docker container'
            }

        }

        stage('Test') {
            steps {
                sh 'echo No tests available'
            }
        }
    }


}