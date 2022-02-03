pipeline {
    agent { label "Slave-1"}

    stages {
        stage('Build') {
            steps {
                bat "docker build -t bhanwardocker/myfirstpipeline E:\\DevOpsDemo\\Jenkins\\Slave-1\\workspace\\myfirstpipeline"
            }
        }
        stage('Clean') {
            steps {
                bat 'docker rm -f mypipelineweb || true..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'docker run -it -d -p 96:80 --name mypipelineweb bhanwardocker/myfirstpipeline'
            }
        }
    }
}