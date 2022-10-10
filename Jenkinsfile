pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                #login ecr
                aws ecr get-login-password --region sa-east-1 | docker login --username AWS --password-stdin 278188084367.dkr.ecr.sa-east-1.amazonaws.com
                #build_image
                docker build -t 278188084367.dkr.ecr.sa-east-1.amazonaws.com/static:$BUILD_NUMBER .
                #push the image to ecr
                docker push 278188084367.dkr.ecr.sa-east-1.amazonaws.com/static:$BUILD_NUMBER

            }
        }
    }
}
