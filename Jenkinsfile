pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('Initial') {
      steps {
        sh 'npm -v'
      }
    }
    stage('Test') {
      steps {
        wrap([$class: 'Xvfb', screen: '1024x768x24']) {
          sh 'npm test'
        }
      }
    }
  }
}