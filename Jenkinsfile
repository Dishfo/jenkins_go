
pipeline {
    agent {
        docker {
            image 'golang:latest'
        }
    }
    stages {
        stage ('Build') {
            steps {
                sh 'echo  BUILD'
                sh 'go version'
                sh 'echo "$PWD"'
                sh 'go build -o J_go'
            }
        }

        stage ('Run') {
            steps {
                sh './J_go'
            }
        }


    }


}
