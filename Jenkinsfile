//Pipeline: Branch type - Basic usage (Declarative Pipeline)
// Using git without checkout 
pipeline {
  agent any
  triggers {
    pollSCM 'H/10 * * * *'
  }
  parameters {
        string(name: 'Git_URL', defaultValue: '', description: 'Who should I say hello to?')
        string(name: 'AWS_CREADS', defaultValue: '', description: 'Who should I say hello to?')
    }
  stages {
    stage('Example') {
      steps {
        withAWS(credentials:"${params.AWS_CREADS}") {
          sh "aws s3 ls"
          
    // do something
        }
        sh " >$WORKSPACE/values.groovy"
        sh "touch $WORKSPACE/values.groovy"
        sh "ls $WORKSPACE/values.groovy"
        sh "echo 'env.giturl=\"${params.Git_URL}\"' >> $WORKSPACE/values.groovy"
        sh "cat $WORKSPACE/values.groovy"
        
        
      }
    }
  }
}
