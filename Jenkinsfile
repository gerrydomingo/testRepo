pipeline {
  agent none
  stages {
    stage('stage1') {
      steps {
        build 'ChoicePointNG'
      }
    }
    stage('stage2') {
      parallel {
        stage('stage2') {
          steps {
            sh 'pwd'
          }
        }
        stage('stage2_1') {
          steps {
            timeout(time: 10) {
              sleep 10
            }

          }
        }
      }
    }
    stage('stage3') {
      steps {
        retry(count: 2) {
          sh 'ls'
        }

      }
    }
  }
}