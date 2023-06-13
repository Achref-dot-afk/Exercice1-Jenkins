pipeline{
    agent any
    environment{
        DOCKERHUB_USERNAME = 'achref2h'
        DOCKERHUB_PASSWORD = 'achreflolh1bli'
    }
    stages{
        stage('Logging in to Docker Hub'){
            steps{
                sh' docker login -u $DOCKERHUB_USERNAME -p $DOCKERHUB_PASSWORD'
                echo ' Logged in successfully '
            }
        }
       
        stage('Building the image'){
            steps{
                sh' docker build -t $DOCKERHUB_USERNAME/my-docker-image:lts .'
                echo 'Image built successfully'
            }
        }
        stage('Pushing the image to Docker Hub'){
            steps{
                sh' docker push $DOCKERHUB_USERNAME/my-docker-image:lts'
                echo 'Image pushed successfully'
            }
        }
    }
}