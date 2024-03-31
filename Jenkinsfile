@Library('jenkins_shared') _
pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Git Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/vigneshwarangappan/jenkinsbuild.git'
            }
        }
    stage('Shared Library Reference'){
            steps{
              sh 'sudo apt update'
              sh    'sudo apt install docker.io '
              dockerBuild() 
            }
        }
        stage('Docker Run'){
            steps{
                sh 'docker run javaapp:latest'
            }
        }     
  }
}
