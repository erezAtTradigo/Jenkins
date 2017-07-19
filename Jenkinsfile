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
        build(job: 'FIXation-tags', propagate: true)
        error 'build failed'
        node(label: 'uat1')
      }
    }
  }
}