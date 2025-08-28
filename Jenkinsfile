pipeline {
  agent any
  options { timestamps(); ansiColor('xterm'); buildDiscarder(logRotator(numToKeepStr: '50')); timeout(time: 30, unit: 'MINUTES') }
  stages {
    stage('Checkout') { steps { checkout scm } }
    stage('Discover services') {
      steps {
        script {
          def dirs = sh(returnStdout: true, script: "ls -1 services || true").trim().split('\n').findAll { it }
          echo "Found services: ${dirs}"
        }
      }
    }
  }
}
