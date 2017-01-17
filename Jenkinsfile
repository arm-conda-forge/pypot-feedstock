#!groovy

// Requires Miniconda with conda-build



pipeline {
	agent label:'' // use any available Jenkins agent

  stage('build') {
    parallel (
      "armv7" : {
        node('armv7') {
        conda build recipe
        }
      }
    )
  }
