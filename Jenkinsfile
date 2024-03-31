@Library('jenkins_shared') _

pipeline{

    agent {  docker { image 'ubuntu:latest' } }
    stages{

        stage('Git Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/vigneshwarangappan/jenkinsbuild.git'
            }
        }
        stage('Shared Library Reference'){
            steps{
            dockerBuild() 
            sh "docker image build -t javaapp:latest "
            }
        }
        stage('Docker Run'){
            steps{
                sh 'docker run javaapp:latest'
            }
        }        
    }
}
