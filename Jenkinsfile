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
        input(message: 'PleaseClickYouInput', ok: 'ButtonOK', id: 'iID', submitter: 'InputSubmitter', submitterParameter: 'InputSubmitterParam')
      }
    }
    stage('SelectedMSG') {
      environment {
        YesOrNo = 'Yes'
      }
      parallel {
        stage('YES') {
          steps {
            echo 'YES'
          }
        }
        stage('NO') {
          steps {
            echo 'NO'
          }
        }
      }
    }
    stage('End') {
      steps {
        echo 'End'
      }
    }
  }
}