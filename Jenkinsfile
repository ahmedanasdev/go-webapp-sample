pipeline {
    agent {
        docker { image 'golang:latest' }
    }
    //tools {go-1/17'}
    //environment {GO111MODULE='on'}
    stages {
        stage('Development') {
        steps {
            git 'https://github.com/ahmedanasdev/go-webapp-sample.git'
            //sh 'go test ./...'
        }
     }
     stage('Building our image') {
        steps {
            script {
                app = docker.build("ahmedanas04/go-webapp-sample:${env.BUILD_ID}")
            }
        }
     }
  }
}