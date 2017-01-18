#!groovy

// Requires Miniconda with conda-build


pipeline {
  agent any // use any available Jenkins agent

  stages {
    stage('build') {
      steps {
        parallel (
          "armv7" : {
            node('armv7') {
              sh 'conda build recipe'
            }
          }
        )
      }
    }
  }
}
