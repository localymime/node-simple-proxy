pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Run Proxy') {
      steps {
        sh 'nohup node app.js > output.log &'
      }
    }
    stage('Testing Proxy') {
      steps {
        sh 'telnet localhost 31330'
      }
    }
  }
}