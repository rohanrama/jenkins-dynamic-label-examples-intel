pipeline {
  agent {
   label createDynamicAnkaNode(
      masterVmId: '9bf0318f-5c58-4142-b544-cf743a087a41',
      tag: 'v2',
      nameTemplate: 'simple-example'
    )
  }
   stages {
     stage("hello") {
       steps {
         sh "echo hello; sleep 120"
       }
     }
  }
  post { always {
    script {
      input(message: "Env is  up for you to take a look at.\nAborting the job at this point will AVOID the cleaning process", ok: "CLEAN THE ENV")
    }
  } }
}
