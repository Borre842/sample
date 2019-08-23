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
        sh 'npm build'
      }
    }
    stage('test') {
      steps {
        sh 'npm test'
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