pipeline {
    agent any

    stages {
        stage("Code Checkout") {
            steps {
                git branch: 'main', url: 'https://github.com/guggilladarshan/Discover-Doller-Assessment-'
            }
        }

        stage("Build Docker Images") {
            steps {
                sh 'docker build -t backend-one ./backend'
                sh 'docker build -t frontend-one ./frontend'
            }
        }

        stage("Tag Images") {
            steps {
                sh 'docker tag backend-one guggilladarshan/backend-one:latest'
                sh 'docker tag frontend-one guggilladarshan/frontend-one:latest'
            }
        }

        stage("Push Images to DockerHub") {
            steps {
                withCredentials([string(credentialsId: 'dockerhub1', variable: 'dckr_pat_X9cQLaSARQUzLbKOZDKDATnckGc')]) {
                    sh 'echo dckr_pat_X9cQLaSARQUzLbKOZDKDATnckGc | docker login -u guggilladarshan --password-stdin'
                    sh 'docker push guggilladarshan/backend-one:latest'
                    sh 'docker push guggilladarshan/frontend-one:latest'
                }
            }
        }

        stage("Deploy") {
            steps {
                sh 'docker stop backend-one frontend-one || true'
                sh 'docker rm backend-one frontend-one || true'

                sh 'docker run -d --name backend-one -p 9090:8080 guggilladarshan/backend-one:latest'
                sh 'docker run -d --name frontend-one -p 80:80 guggilladarshan/frontend-one:latest'
            }
        }
    }
}
