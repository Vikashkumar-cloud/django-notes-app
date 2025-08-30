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
        stage("Code Build"){
            steps{
            dockerbuild("notes-app","latest")
            }
        }
        stage("Push to DockerHub"){
            steps{
                dockerpush("dockerHubCreds","notes-app","latest")
            }
        }
        stage("Deploy"){
            steps{
                deploy()
            }
        }
    }
}
