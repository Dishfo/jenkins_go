
pipeline {
    agent {
        dockerfile {
            image 'golang:latest'
        }
    }
    stages {
        stage ('Build') {
            steps {
                sh 'echo  BUILD'
                sh 'go version'
                sh 'echo "$PWD"'

                sh 'file=${PWD##*/}'
                sh 'cd "${GOPATH}/src"'
                sh 'git clone "${GIT_URL}"'
                sh 'cd jenkins_go'
                sh 'go build -o j_go'
            }
        }

        stage ('Run') {
            steps {
                sh './j_go'
            }
        }
    }


}
