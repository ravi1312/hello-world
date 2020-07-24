//Pipeline: Branch type - Basic usage (Declarative Pipeline)
// Using git without checkout 
pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        load "$WORKSPACE/values.groovy"
        echo "${env.Git_URL_API}"
        echo "${env.Git_Token}"
        sh "git push https://${env.Git_Token}@${env.Git_URL_API}"
      }
    }
  }
}
