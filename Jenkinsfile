#!groovy

// Requires Miniconda with conda-build


pipeline {
  stage('build') {
    parallel (
      "armv7" : {
        node('armv7') {
          sh 'conda build recipe'
        }
      }
    )
  }
}
