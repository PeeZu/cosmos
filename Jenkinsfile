pipeline {
  agent none
  stages {
    stage('baseline') {
      steps {
        echo 'Baseline stage'
      }
    }
    stage('') {
      steps {
        sleep 2
        timeout(time: 5) {
          echo 'migrate'
        }

      }
    }
  }
}