#!groovy

pipeline {

  agent none

  options {
    buildDiscarder(logRotator(numToKeepStr: '10'))
    skipDefaultCheckout()
    timeout(time: 4, unit: 'HOURS')
    timestamps()
  }

  stages {
    stage('cypress Tests') {
        when {
            anyOf {
                branch 'master'
            }
        }

        steps {
            checkout scm
        }
    }
  }
}