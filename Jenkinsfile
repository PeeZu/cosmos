pipeline {
  agent none
  stages {
    stage('baseline') {
      parallel {
        stage('baseline') {
          steps {
            echo 'Baseline stage'
          }
        }
        stage('privilege') {
          steps {
            echo 'test'
          }
        }
        stage('schema') {
          steps {
            echo 'schema'
          }
        }
        stage('dependency') {
          steps {
            echo 'dependency'
          }
        }
      }
    }
    stage('migrate') {
      parallel {
        stage('migrate') {
          steps {
            sleep 2
            echo 'migrate stage'
          }
        }
        stage('local') {
          steps {
            echo 'local'
          }
        }
        stage('pending') {
          environment {
            FOO = 'bar'
          }
          steps {
            echo 'pending'
          }
        }
      }
    }
    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            sleep 2
          }
        }
        stage('cleanup') {
          steps {
            echo 'cleanup'
          }
        }
      }
    }
    stage('test') {
      steps {
        echo 'test'
      }
    }
  }
}