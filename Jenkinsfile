pipeline{
    agent any
    stages{
        stage("Pull latest image"){
            steps{
                bat "docker pull nuclearfanta/selenium-docker"
            }
        }
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
    }
        post{
            always{
                archiveArtifacts artifacts: 'output/**'
                bat "docker-compose down"
            }
        }
    

}