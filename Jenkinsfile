@Library('jenkins-shared-lib') _
pipeline {
    agent any
    
    stages {
        stage("Git Clone"){
           steps {
               script{
                  clone ("https://github.com/Vikashkumar-cloud/django-notes-app.git","main")
               }
            } 
        }
    }
}
