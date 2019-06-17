// Using git without checkout
pipeline {
  agent any
  parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH'
  }
  stages {
    stage('check out') {
      checkout scm: [$class: 'GitSCM', branches: [[name: "refs/heads/${params.BRANCH}"]]] 
    }
  }
}