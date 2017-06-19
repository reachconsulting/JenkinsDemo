pipeline {
  agent any
  stages {
    stage('build1') {
      steps {
        parallel(
          "build1": {
            sh 'sh ./build1'
            
          },
          "build2": {
            sh 'sh ./build2'
            
          },
          "build3": {
            sh 'sh ./build3'
            
          },
          "build4": {
            sh 'sh ./build4'
            
          }
        )
      }
    }
  }
}