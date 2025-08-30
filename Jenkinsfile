pipeline {
    agent any
    
    stages {
        stage("Git Clone"){
           steps {
               git branch: 'main', url: 'https://github.com/Vikashkumar-cloud/django-notes-app.git'
           } 
        }
        stage("Docker Build"){
           steps {
               sh 'whoami'
               sh 'docker build -t notes-app .'
           } 
        }
        stage("Docker Push"){
           steps {
               echo 'Docker image has been push'
           } 
        }
        stage("Deploy"){
           steps {
               sh 'docker compose down && docker compose up -d'
           } 
        }
    }
}
