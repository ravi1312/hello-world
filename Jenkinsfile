//Pipeline: Branch type - Basic usage (Declarative Pipeline)
// Using git without checkout 
pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        load "$WORKSPACE/values.groovy"
        echo "${env.Git_URL}"
        echo "${env.Git_Token}"
      }
    }
  }
}
