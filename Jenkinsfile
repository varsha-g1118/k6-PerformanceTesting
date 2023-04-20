pipeline {
  agent any
  stages {
    stage('verify k6') {
      steps {
        sh 'xk6 version'
      }
    }
    stage('run k6 test') {
      steps {
        sh 'xk6 run --vus 10 --duration 30s --out influxdb=http://192.168.0.107:8086 demok6.js'
      }
    }
  }
}
