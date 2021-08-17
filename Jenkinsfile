@Library('Piper_lib_abap') _
node(jenkins233slave){
  stage('Prepare')   {
      checkout scm
      abapEnvironmentPipeline script: this
  }
}
