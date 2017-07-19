pipeline {
  agent any
  stages {
    stage('init') {
      steps {
        echo 'test init pipeline'
        build 'FIXation-Env'
      }
    }
    stage('build') {
      steps {
        build(job: 'FIXation-tags', propagate: true)
        error 'build failed'
        node(label: 'uat1')
      }
    }
  }
}