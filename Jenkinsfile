pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
               
                sh 'aws ecr get-login-password --region sa-east-1 | sudo docker login --username AWS --password-stdin 278188084367.dkr.ecr.sa-east-1.amazonaws.com'
                
                sh 'sudo docker build -t 278188084367.dkr.ecr.sa-east-1.amazonaws.com/static:$BUILD_NUMBER .'
                
                sh 'sudo docker push 278188084367.dkr.ecr.sa-east-1.amazonaws.com/static:$BUILD_NUMBER'

            }
        }
    }
}
