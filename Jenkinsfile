pipeline {
    agent {
        docker { image 'golang:latest' }
    }
    //tools {go-1/17'}
    //environment {GO111MODULE='on'}
    stages {
        stage('Test') {
        steps {
            git 'https://github.com/ahmedanasdev/go-webapp-sample.git'
            sh 'go test ./...'
        }
     }
  }
}