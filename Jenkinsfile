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
        build job: 'FIXation-CentOS7', parameters: [[$class: 'ListSubversionTagsParameterValue', name: 'SVN_TAG', tag: 'trunk', tagsDir: 'svn://infra.fluent.local/jcfx']]
        //build 'FIXation-tags'
        error 'build failed'
      }
    }
  }
}
