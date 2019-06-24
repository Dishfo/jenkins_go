
pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                sh 'echo  BUILD'
                sh 'go version'
                sh 'echo "$PWD"'
                sh 'env'

                sh 'cp -r "$PWD" "${GOPATH}/src"'
                sh 'cd "${GOPATH}/src/${PWD##*/}"'
                sh 'go build -o j_go'
            }
        }

        stage ('Build') {
            steps {
                sh './j_go'
            }
        }
    }


}
