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
            agent {
                dockerfile {
                    label'app-template'

                }
            }

            steps{
                sh 'docker run -p 8081:8081 -rm app-template'
                sh 'docker stop app-template'
            }

        }

        stage('Test') {
            steps {
                sh 'echo No tests available'
            }
        }
    }


}