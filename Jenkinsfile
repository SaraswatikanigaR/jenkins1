pipeline{
    agent any

    environment{
        DOCKER='"C:\\Progarm Files\\Docker\\Docker\\resource\\bin\\docker.exe"'
    }

    stages{
        stage('Build Docker Image'){
            steps{
                bat '%DOCKER% build -t python-app .'

            }
        }
    }
        
    stages{
        stage('Run Tests Inside Docker'){
            steps{
                bat '%DOCKER% run --rm python-app pytest'

            }
        } 
    }
    stages{
        stage('Run Application'){
            steps{
                bat '%DOCKER% run --rm python-app'

            }
        } 
    }

        

    }
