pipeline {
  agent any
  stages {
    stage('Build') {
      steps { sh 'docker build -t mysite .' }
    }
    stage('Test') {
      steps { sh 'grep "<h1>" index.html' }
    }
    stage('Deploy') {
      steps {
        sh 'docker rm -f mysite || true'
        sh 'docker run -d -p 80:80 --name mysite mysite'
      }
    }
  }
}
