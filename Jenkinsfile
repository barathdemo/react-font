pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/barathdemo/react-font.git'
            }
        }
        stage('Docker Build') {
            steps {
                script {
                    sh 'docker build -t 181098/test-guvi:2 .'
                }
            }
        }
        stage('Docker Push') {
            steps {
                script {
                    sh 'docker push 181098/test-guvi:2'
                }
            }
        }
    }
}
