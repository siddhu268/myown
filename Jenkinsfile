pipeline {
  agent any
  stages {
    stage('pull') {
      steps {
        sh 'mvn clean test -DskipTests'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn deploy'
      }
    }
  }
}