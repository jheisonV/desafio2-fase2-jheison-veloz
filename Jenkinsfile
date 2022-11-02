pipeline {
    agent any
    stages {
        stage('AWS VALIDATE') {
            steps {
                echo 'AWS STS'
                sh 'aws sts get-caller-identity'
            }
        }
        stage('AWS S3 listar') {
            steps {
                sh 'aws s3 ls'
            }
        } 
        stage('Git Clone') {
            steps {
                sh '''rm -rf jhei-bootcamp/'''
                sh 'git clone https://github.com/jheisonV/jhei-bootcamp.git'
                sh 'ls -lrt jhei-bootcamp/'
            }
        } 
        stage('Upload to S3') {
            steps {
                sh 'aws s3 cp jhei-bootcamp s3://pagina-jh --recursive'
            }
        }         
    }
}
