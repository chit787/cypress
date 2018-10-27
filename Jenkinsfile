#!groovy

pipeline {

  agent any

  options {
    buildDiscarder(logRotator(numToKeepStr: '10'))
    skipDefaultCheckout()
    timeout(time: 4, unit: 'HOURS')
    timestamps()
  }

  stages {
    stage('cypress Tests') {
        steps {
            checkout scm
            sh 'echo 1'
        }
    }
  }
}
