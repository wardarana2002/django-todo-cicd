pipeline {
  agent { dockerfile true }
  stages {
    stage('Test') {
      steps {
        docker build -t todo .
        docker run -d -p 8000:8000 todo
      }
    }
  }
}
