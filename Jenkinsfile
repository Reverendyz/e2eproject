pipeline {
    agent any

    environment {
        BASE_IMAGE='base-image/Dockerfile'
        CREDS=environment('reverendyz-creds')
    }

    stages{
        stage('Build image'){
            steps{
                sh 'docker build -t reverendyz/e2etool:latest -f ${BASE_IMAGE}'
            }
        }
        stage('Login to docker registry'){
            steps{
                sh 'echo ${CREDS_PSW} | docker login -u ${CREDS_USR} --password-stdin'
            }
        }
    }
    //TODO
}