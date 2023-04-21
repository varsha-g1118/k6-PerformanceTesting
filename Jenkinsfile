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
        sh 'k6 run --vus 10 --duration 30s --out influxdb-1=http://192.168.0.107:8086/k6 demok6.js'
      }
    }
  }
}
