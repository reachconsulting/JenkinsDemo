pipeline {
  agent any
  stages {
    parallel(
      stage('component1') {
        steps {
          "build1": {
            sh 'sh ./build1'
          },
          "unittest1": {
            sh 'sh ./unittest2'
            
          }
        }
      },
      stage('component2') {
        steps {
          "build2": {
            sh 'sh ./build2'
          },
          "unittest2": {
            sh 'sh ./unittest2'
            
          }
        }
      }
    )
    stage('integration1') {
        steps {
          "integration1": {
            sh 'sh ./integration1'
          },
        }
      )
    }

  }
}