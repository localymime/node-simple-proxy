pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'node app.js'
      }
    }
    stage('Testing Proxy') {
      steps {
        sh 'telnet localhost 31330'
      }
    }
  }
}