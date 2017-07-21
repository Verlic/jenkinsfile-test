pipeline {
    agent any
    tools { nodejs 'node-v6.10.3' }
    parameters {
        string(name: 'REGION', defaultValue: 'us-west-1', description: 'The region to deploy')
    }
    stages {
        stage('deploy-us') {
            when {
                expression { return params.REGION == 'us-west-1' }
            }
            steps {
                echo "${REGION}"
            }
        }
        
        stage('deploy-eu') {
            when {
                expression { return params.REGION == 'eu-central-1' }
            }
            steps {
                echo "${REGION}"
            }
        }
        
        stage('deploy-au') {
            when {
                expression { return params.REGION == 'ap-southeast-2' }
            }
            steps {
                echo "${REGION}"
            }
        }
    }
}
