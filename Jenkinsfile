pipeline {
  agent { dockerfile true }
  stages {
    stage('Test') {
      steps {
        sh '''
          sudo docker build -t todo .
          sudo docker run -d -p 8000:8000 todo 
        '''
      }
    }
  }
}
