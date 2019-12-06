pipeline {
   agent any

   stages {
      stage('Build Apk') {
         steps {
        bat "gradlew clean"
        bat "gradle build"
         }
      }
   }
   post {
           always {
               emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
           }
       }
}