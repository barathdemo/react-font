pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/barathdemo/react-font.git'
            }
        }
        stage('Docker Build') {
            steps {
                script {
                    sh 'docker build -t barath2707/docker:$BUILD_NUMBER .'
                }
            }
        }
        stage('Docker Push') {
            steps {
                script {
                    sh 'docker push barath2707/docker:$BUILD_NUMBER'
                }
            }
        }
    }
}
