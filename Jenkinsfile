pipeline {
    agent {
        docker { image 'golang:1.17' }
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