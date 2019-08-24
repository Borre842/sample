pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Install') {
      agent {
        docker {
          args '-p 3000:3000 '
          image 'node:6-alpine'
        }

      }
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
        emailext(subject: 'Test devops jenkins', body: 'bla bla bla', attachLog: true, to: '0001testingemail001@gmail.com')
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