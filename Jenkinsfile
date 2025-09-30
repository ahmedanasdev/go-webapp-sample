pipeline {
    agent any//{
        //docker { image 'golang:latest' }
    //}
    tools {
        go 'go-1.22'
    }
    //environment {GO111MODULE='on'}
        stages {
            stage('Test') {
            steps {
                git 'https://github.com/ahmedanasdev/go-webapp-sample.git'
                sh 'go test ./...'
            }
        }
        stage('Build and Run') {
            steps {
                //git 'https://github.com/ahmedanasdev/go-webapp-sample.git' تجربه انى عامل كلون فوق 
                sh 'go build .'
                sh './go-webapp-sample' 
                }
            }
            stage('Run'){
                steps{
                    sh 'cd /var/lib/jenkins/workspace/go-full-pipeline && go-webapp-sample &'
                }
            }
     }
  }
