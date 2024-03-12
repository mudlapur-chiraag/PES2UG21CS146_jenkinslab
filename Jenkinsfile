pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS146-1'
          echo "Building..."
          sh 'g++ main/hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        echo "Testing..."
        sh './output'
      }
    }
    stage('Deploy') {
      script {
        echo 'Deploying...'
      }
    }
  }
}
post {
    failure {
        echo 'Pipeline failed'
      }
    }
  }
