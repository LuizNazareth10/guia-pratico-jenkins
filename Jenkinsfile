pipeline{
    agent any

    stages{
        stage('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("luiznazareth/guia-jenkins:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')
                }
            }
        }
        stage('Push Docker Image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        dockerapp.push('latest')
                        dockerapp.push("${env.BUILD_ID}")
                    }
                }
            }
        }
        stage('Deploy no Kubernetes') {
            steps {
                sh 'echo "Deploying to Kubernetes..."'
                // Add your deployment commands here
            }
        }
    }
}