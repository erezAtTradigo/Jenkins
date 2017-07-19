pipeline {
  agent any
  stages {
    stage('init') {
      steps {
        echo 'test init pipeline'
      }
    }
    stage('build') {
      steps {
        build 'FIXation-tags'
        error 'build failed'
      }
    }
  }
}