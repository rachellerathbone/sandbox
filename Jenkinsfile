pipeline {
     agent any
     stages {
         stage('Build') {
             steps {
                 echo 'Building...'
             }
             post {
                 always {
                     jiraSendBuildInfo branch: '', site: 'rachellerathbone.atlassian.net'
                 }
             }
         }
     }
 }
