pipeline{
    agent any

    stages{
        stage('Build Docker Image') {
            steps {
                sh 'echo "Building Docker Image..."'
                // Add your build commands here
            }
        }
        stage('Push Docker Image') {
            steps {
                sh 'echo "Pushing Docker Image to Registry..."'
                // Add your push commands here
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