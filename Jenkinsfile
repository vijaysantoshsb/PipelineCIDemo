pipeline {
   agent any

   stages {
      stage('Build Apk') {
         steps {
        bat "gradlew build"
      
         }
      }
   }
   post {
           always {
               emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
           }
       }
}
