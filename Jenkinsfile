pipeline{
  agent { docker { image 'bryandollery/terraform-packer-aws-alpine ' } }
  options {
    skipStagesAfterUnstable()
 }
 stages {
  stage('BuildStaging') {
   steps {
     sh 'docker build --tag bryan:$BUILD_NUMBER' 
 }
}
 stage('DeployStaging'){
   steps {
     echo 'deploying application on staging environment'
 }
} 
stage('ValidateStageDeployment') {
 steps {
    echo 'validate deployment on staging'
     }
    }
  }
 }
