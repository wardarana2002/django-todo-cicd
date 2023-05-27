pipeline {
  agent any
  stages {
    stage('Build') {
     agent {
        docker { image 'django:latest' }
      }
      steps {
        sh 'python3 manage.py'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker build -t todo .'
        sh 'docker run -d -p 8000:8000 todo'
      }
  }
}
}
