pipeline{
    agent any
    stages{
        stage("Run test"){
            steps{
                bat "docker-compose up"
            }
        stage("Bring Grid down"){
            steps{
                bat "docker-compose down"
            }
        }
        }

    }
}