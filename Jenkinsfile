pipeline {
    stages {
        stage('Build'){
            sh './gradlew build'
        }
        stage('Spin up Container'){
            agent { dockerfile{
                additionalBuildArgs '-p 8081:8081'
            } }

        }

        stage('Test') {
            steps {
                sh 'echo No tests available'
            }
        }
    }


}