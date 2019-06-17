#!/usr/bin/groovy

def label = "worker-${UUID.randomUUID().toString()}"


// INPUT PARAMETERS
properties([
  parameters([
    gitParameter(name: 'BRANCH_NAME', defaultValue: 'master', selectedValue: 'DEFAULT', type: 'PT_BRANCH'),
   ])
])

node("master") {
  stage('check out') {
    checkout scm: [$class: 'GitSCM', branches: [[name: "refs/heads/${params.BRANCH}"]]] 
    }
  }
