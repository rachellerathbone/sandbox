pipeline {
     agent any
     stages {
         stage('Build') {
             steps {
                 echo 'Building...'
                 throw new Exception("Throw to stop pipeline")
             }
             post {
                 always {
                     jiraSendBuildInfo site: 'rachellerathbone.atlassian.net'
                 }
             }
         }
     }
 }
