@Library('jenkins_shared') _

pipeline{

    agent any
    stages{
         
        stage('Git Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/vigneshwarangappan/jenkinsbuild.git'
                git clone
            
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
