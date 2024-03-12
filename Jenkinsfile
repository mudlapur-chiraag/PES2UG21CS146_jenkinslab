pipeline {
    agent any
  
    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS146-1'
                echo 'Building...'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                    echo 'Testing...'
                    sh './output'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'Output'
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
