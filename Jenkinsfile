pipeline {
  agent any
  stages {
    stage('Build stage') {
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
    stage('Packaging stage') {
      steps {
        sh 'echo "packaging..."'
      }
    }   
    stage('UT stage') {
      steps {
        parallel(
          "unittest1": {
            sh 'sh ./unittest1'
            
          },
          "unittest2": {
            sh 'sh ./unittest2'
            
          },
          "unittest3": {
            sh 'sh ./unittest3'
            
          },
          "unittest4": {
            sh 'sh ./unittest4'
            
          }
        )
      }
    }
    stage('Integration stage') {
      steps {
        parallel(
          "integration1": {
            sh 'sh ./integration1'
            
          },
          "integration2": {
            sh 'sh ./integration2'
            
          }
        )
      }
    }
    stage('systemTest stage') {
      steps {
        sh 'sh ./systemTest'
      }
    }
  }
}