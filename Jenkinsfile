pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
                checkout scm
            }
        }
        stage('Build docker image'){
            steps{
                bat 'docker build -t myapp .'
            }
        }
        stage('Deploy'){
            steps{
                bat 'docker run -d -p 3010:3000 --name myapp myapp'
            }
        }
    }
}