pipeline{
    agent any
    stages{
        stage("start Grid"){
            steps{
                bat "docker-compose up -d hub firefox chrome"
            }
        }
        stage("Run Tests"){
            steps{
                bat "docker-compose up book-flight-module search-module"
            }
        }
        stage("Bring Grid down"){
            steps{
                bat "docker-compose down"
            }
        }
    }

}