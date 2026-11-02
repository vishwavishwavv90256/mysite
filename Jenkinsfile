pipeline {
  agent any
  stages {
    stage('Get code') {
      steps {
        echo 'Code received from GitHub'
      }
    }
    stage('Build') {
      steps {
        sh 'ls'
        sh 'cat index.html'
      }
    }
    stage('Test') {
      steps {
        sh 'grep "<h9>" index.html'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying website...'
      }
    }
  }
}
