pipeline {
     agent any
     stages {
         stage ('Upload to AWS') {
             steps {
                  withAWS(region:'eu-west-3', credentials:'aws-static') {
                 sh 'echo "Hello World"'
                       s3Upload(file:'index.html', bucket:'myjenkinsbucket25') {
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
                     }
                 }       
             }
          }
      }
}
