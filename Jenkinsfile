pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('test') {
      steps {
        sh 'npm test'
        emailext(subject: 'Test devops jenkins', body: 'bla bla bla', attachLog: true)
      }
    }
    stage('aprove') {
      steps {
        input(message: 'this work?', submitter: 'gera842')
      }
    }
    stage('deploy') {
      steps {
        echo 'Print message egb'
      }
    }
  }
}