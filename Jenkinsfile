pipeline{
    agent any
    environment{
        DOCKERHUB_USERNAME = credentials('dockerhub-username')
        DOCKERHUB_PASSWORD = credentials('dockerhub-password')
    }
    stages{
        stage('Logging in to Docker Hub'){
            steps{
                sh' docker login -u $DOCKERHUB_USERNAME -p $DOCKERHUB_PASSWORD'
            }
        }
        stage('Building the image'){
            steps{
                sh' docker build -t $DOCKERHUB_USERNAME/my-docker-image:latest .'
                echo 'Image built successfully'
            }
        }
    }
}