
node {

  stage('Preparation') { // for display purposes

     git 'https://github.com/Eugene2011/spring-petclinic.git'
   
  }
  stage('Build') {
           sh './mvnw -Dmaven.test.failure.ignore verify'
  }
  stage('Results') {
     junit ''**/target/surefire-reports/TEST-*.xml'
     archiveArtifacts 'target/*.jar'
  }
}
