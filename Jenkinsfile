pipeline {
  agent any
  triggers {
    pollSCM('H/2 * * * *') 
  }
  stages {
    stage('pull') {
      steps {
        sh 'mvn -f exchangerate-papi/pom.xml clean test -DskipTests'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn -f exchangerate-papi/pom.xml deploy -DskipTests'
      }
    }
  }
}
