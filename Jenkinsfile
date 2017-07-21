pipeline {
  agent any
  stages {
    stage('deploy-us') {
      when {
        expression {
          return params.REGION == 'us-west-1'
        }
        
      }
      steps {
        parallel(
          "deploy-us": {
            echo '"${REGION}"'
            
          },
          "deploy-region": {
            echo 'hello world'
            
          }
        )
      }
    }
  }
  tools {
    nodejs 'node-v6.10.3'
  }
  parameters {
    string(name: 'REGION', defaultValue: 'us-west-1', description: 'The region to deploy')
  }
}