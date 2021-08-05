@Library('piper-lib-os@v1.53.0') _
node('jenkins233slave'){
  stage('Prepare')   {
      cloudFoundryCreateServiceKey script: this
      abapEnvironmentPipeline script: this
  }

  stage('Build')   {
      mtaBuild (
      script:this )
  }

  stage('Deploy')   {
      cloudFoundryDeploy(
      script:this, 
      verbose:true)
  }
}
