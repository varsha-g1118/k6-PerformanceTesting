pipeline {
  agent any
  stages {
    stage('verify k6') {
      steps {
        sh 'k6 version'
      }
    }
    stage('run k6 test') {
      steps {
        sh 'k6 run --vus 10 --duration 30s demok6.js'
      }
    }
  }
}
