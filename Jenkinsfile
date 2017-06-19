pipeline {
  agent any
  stages {
    stage('build & unit') {
      steps {
        parallel(
          steps{
            "build1": {
              sh 'sh ./build1'
            },
            "unittest1": {
              sh 'sh ./unittest1'
            },
          }
          steps{
            "build2": {
              sh 'sh ./build2'
            },
            "unittest1": {
              sh 'sh ./unittest2'
            },
          }
        )
      }
    }
  }
}