pipeline {
    agent  any
    stages {
        stage('deployments') {
            parallel {
                stage('deploy to stg') {
                    steps {
                        echo 'stg deployment done'
                    }
                }
                stage('deploy to prod') {
                    steps {
                        echo 'prod deployment done'
                    }
                }
            }
           post {
                 always {
                     jiraSendBuildInfo branch: 'main'
                 }
             }
        }
    }
}
