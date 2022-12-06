pipeline {
    agent any
    stages {
        stage ("Clone git repo") {
            steps{
                git branch: 'main'
                    url: https://github.com/boorgu123/Project_fall.git
                sh "ls -lat"
            }
        }
    }
        stage("AWS CFT") {
            steps{
                 aws cloudformation create-stack \
                 --stack-name EC2instance.yaml \
                 --template-body EC2instance.yaml \
            }
        }
}
}
