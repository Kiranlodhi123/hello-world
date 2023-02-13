pipeline {
  agent any
  stages {
    stage('git checkout') {
      parallel {
        stage('git checkout') {
          steps {
            echo 'hello git'
          }
        }

        stage('check parallel ') {
          steps {
            sh '''pwd
ls -ltrh
whoami'''
          }
        }

      }
    }

    stage('build') {
      steps {
        sleep 4
      }
    }

    stage('deploy') {
      steps {
        retry(count: 3) {
          echo 'hello '
        }

      }
    }

  }
}