pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
               
                aws ecr get-login-password --region sa-east-1 | sudo docker login --username AWS --password-stdin 278188084367.dkr.ecr.sa-east-1.amazonaws.com
                
                docker build -t 278188084367.dkr.ecr.sa-east-1.amazonaws.com/static:$BUILD_NUMBER .
                
                docker push 278188084367.dkr.ecr.sa-east-1.amazonaws.com/static:$BUILD_NUMBER

            }
        }
    }
}
