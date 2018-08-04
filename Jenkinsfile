#!groovy

pipeline {

  agent none

  options {
    buildDiscarder(logRotator(numToKeepStr: '10'))
    skipDefaultCheckout()
    timeout(time: 4, unit: 'HOURS')
    timestamps()
    ansiColor('xterm')
  }

  stages {
    stage('cypress Tests') {
        when {
            anyOf {
                branch 'master'
            }
        }

        tools {
            jdk 'JDK 8u60'
        }

        steps {
            checkout scm
            dir('stash') {
                unstash name: 'serverZip'
            }
            sh './gradlew apiTest -PuseDistributionLocation=stash'
        }

        post {
            always {
                script {

                }
            }
            failure {

            }
            success {

            }
        }
    }
  }
}