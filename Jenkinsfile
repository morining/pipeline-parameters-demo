#!/usr/bin/groovy

def label = "worker-${UUID.randomUUID().toString()}"
pipeline {
  agent any
  parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH'
  }

   node(label) {

     stage('check out') {
       checkout scm: [$class: 'GitSCM', branches: [[name: "refs/heads/${params.BRANCH}"]]] 
      }
   }
}