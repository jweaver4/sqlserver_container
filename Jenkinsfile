#!/usr/bin/env groovy
node (label: 'linux-agent-1') {
def app = ''

// def servicePrincipalId = 'c5ddf1a8-940f-4817-9afd-86c8a6990332'
// def resourceGroup = 'ARMY-DEMO2-VA'
//def aks = 'ARMY-DEMO-AKS'

def resourceGroup = 'DSO-DEMO-Containers-VA'
def aks = 'DSO-DEMO-AKS'

  stage('Clone repository') {
      checkout scm
  }

  stage('Test image') {

  }

  stage("Build & Push to ACR") {

   }

   stage("Deploy") {
    acsDeploy azureCredentialsId: 'AKSClusterSP',
                  resourceGroupName: resourceGroup,
                  containerService: "${aks} | AKS",
                  configFilePaths: 'sql2017_demo.yaml',
                  enableConfigSubstitution: true
   }
}
