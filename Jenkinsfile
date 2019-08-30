node {
      stage('Preparation')
         { // for display purposes
            git 'https://github.com/Eugene2011/spring-petclinic.git'

         }
   stage('Build') {
      // Run the maven build
                           sh './mvnw -Dmaven.test.failure.ignore clean package'
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts 'target/*.jar'
   }

   stage('Results') {
    emailtext body: 'Отработал.', subject: 'Отбивка текста', to: 'eugene@ekat.ru'
  }
}
