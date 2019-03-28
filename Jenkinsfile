pipeline {
  agent any
  stages {
    stage('pull') {
      steps {
        git(url: 'https://github.com/siddhu268/myown.git', branch: 'master', changelog: true, poll: true, credentialsId: '410f22ac01bd9257ece94045c8a13034fce24cb6')
        sh 'mvn clean test'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn deploy'
      }
    }
  }
}