//@Library('jenkins-shared') _

pipeline{

    agent any
    stages{
         
        stage('Git Checkout'){
            steps{
            gitCheckout(
                branch: "main",
                url: "https://github.com/vigneshwarangappan/jenkinsbuild.git"
            )
            }
        }
        stage('Shared Library Reference'){
            steps{
            dockerBuild()
            }
        }
//        stage('Docker Image Build'){
  //          steps{
    //           script{             
             //      dockerBuild()
              // }
            //}
        //}       
    }
}
