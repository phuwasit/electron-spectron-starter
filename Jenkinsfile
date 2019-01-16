pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage('NPM Setup') {
      steps {
        sh 'npm install'
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