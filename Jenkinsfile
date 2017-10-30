pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        echo 'Start Init Step'
      }
    }
    stage('ManualStep') {
      steps {
        input(message: 'PleaseType', ok: 'ButtonOK', id: 'ID', submitter: 'InputSubmitter', submitterParameter: 'InputSubmitterParam')
      }
    }
  }
}