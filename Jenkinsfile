pipeline {
   agent any
   environment {
     Name = "test"
   }
    stages {
         stage('Cloning Git') {
           steps {
               git "https://github.com/mendelor/jenkins_multi-branch.git"
           }
         }

     stage('Build image') {
       steps {
         script {
               myapp = docker.build("${Name}:${env.BUILD_ID}")
         }
        }
      }
    }
  }
