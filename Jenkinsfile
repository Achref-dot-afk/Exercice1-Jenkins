pipeline{
    agent any
    environment{
        DOCKERHUB_USERNAME = credentials('dockerhub-username')
        DOCKERHUB_PASSWORD = credentials('dockerhub-password')
    }
    stages{
        stage('Building the image'){
            steps{
                sh' docker build -t $DOCKERHUB_USERNAME/my-docker-image:lts .'
                echo 'Image built successfully'
            }
        
        }
        stage('Pushing the app'){
            steps{
                sh'docker push $DOCKERHUB_USERNAME/my-docker-image:latest
                echo ' check your dockerhub account... '
            }
        }
    }
}
