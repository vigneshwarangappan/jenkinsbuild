@Library('jenkins_shared') _

pipeline{

    agent any
    stages{

        stage('Git Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/vigneshwarangappan/jenkinsbuild.git'
            }
        }
        stage('Shared Library Reference'){
            steps{
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
