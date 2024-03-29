@Library('jenkins-shared') _

pipeline{

    agent any
    stages{
         
        stage('Git Checkout'){
            steps{
            gitCheckout(
                branch: "main",
                url: "https://github.com/vigneshwarangappan/jenkins_shared.git"
            )
            }
        }
        stage('Docker Image Build'){
            steps{
               script{
                   
                   dockerBuild()
               }
            }
        }       
    }
}
