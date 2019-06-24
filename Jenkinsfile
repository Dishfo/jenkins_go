
pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                sh 'echo  BUILD'
                sh 'go version'
                sh 'echo "$PWD"'
                sh 'go build -o J_go'
                sh './J_go'
            }
        }


    }


}
