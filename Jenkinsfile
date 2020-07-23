//Pipeline: Branch type - Basic usage (Declarative Pipeline)
// Using git without checkout 
pipeline {
  agent any
  parameters {
    //gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH'
    listGitBranches(parameterType: 'Branch', credentialId: '[testing-git]', repositoryUrl: '[https://github.com/ravi1312/hello-world.git]', name: 'branch')
  }
  stages {
    stage('Example') {
      steps {
        git branch: "${params.BRANCH}", url: 'https://github.com/jenkinsci/git-parameter-plugin.git'
        echo "${params.branch}
      }
    }
  }
}
