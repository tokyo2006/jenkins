pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'git@github.com:BaiwangTradeshift/SC-Backend-Common.git', branch: 'master', changelog: true, poll: true)
      }
    }
    stage('build') {
      steps {
        tool 'maven'
        sh 'mvn clean install'
      }
    }
  }
}