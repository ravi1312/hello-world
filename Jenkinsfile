//Pipeline: Branch type - Basic usage (Declarative Pipeline)
// Using git without checkout 
pipeline {
  agent any
  triggers {
    pollSCM 'H/10 * * * *'
  }
  parameters {
    //gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH'
   // listGitBranches(parameterType: 'BRANCH', credentialsId: 'testing-git', remoteURL: 'https://github.com/ravi1312/hello-world.git', name: 'branch')
    gitParameter(branch: '',
                     branchFilter: 'origin/(.*)',
                     defaultValue: 'master',
                     description: '',
                     name: 'BRANCH',
                     quickFilterEnabled: false,
                     selectedValue: 'NONE',
                     sortMode: 'NONE',
                     tagFilter: '*',
                     type: 'PT_BRANCH')
  }
  stages {
    stage('Example') {
      steps {
        git branch: "${params.BRANCH}", url: 'https://github.com/jenkinsci/git-parameter-plugin.git'
        echo "${params.branch}"
      }
    }
  }
}
pipeline{
  agent any
  stages{
    stage("test"){
      steps{
        echo "hello"
      }
    }
  }
}
