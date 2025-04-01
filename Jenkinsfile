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
         stage('Docker Pull') {
            steps {
                script {
                    sh 'docker pull barath2707/docker:$BUILD_NUMBER'
                }
            }
        }
        stage('Docker Ps') {
            steps {
                script {
                    sh ' docker pa -a'
                }
            }
        }
         stage('Docker ContainerRun') {
            steps {
                script {
                    sh ' docker run -d -p 8090:80 barath2707/docker:$BUILD_NUMBER'
                }
            }
        }
    }
}
