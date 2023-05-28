pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
         sh 'docker build -t todo .'
         sh 'docker run -d -p 8000:8000 todo'
      }
    }
    stage('Test') {
      steps {
       
      }
  }
}
}
