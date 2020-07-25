//Pipeline: Branch type - Basic usage (Declarative Pipeline)
// Using git without checkout 
pipeline {
  agent any
  parameters {
        string(name: 'Git_URL', defaultValue: '', description: 'Who should I say hello to?')
    }
  stages {
    stage('Example') {
      steps {
        sh "echo 'env.giturl="\"${params.Git_URL}"\"'"
      }
    }
  }
}
