node ('HRMS && QA') {
// This illustrates the use of the node, which node to use.

  stage ('git VCS') {
      git 'https://github.com/mitchelwize77/spring-petclinic.git'
  }

  stage ('build') {
      sh 'mvn clean package'
  }

  //stage ('Test Reports') {
     junit 'spring-petclinic/target/surefire-reports/*.xml'
     // '**/surefire-reports/*.xml'
  }  
  
 // stage ('Archive the Artifacts') {
      artifacts: '**/target/*.war'
  }
  
} 