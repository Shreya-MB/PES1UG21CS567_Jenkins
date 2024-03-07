pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES1Ug21CS567-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'display'
      }
    }
  }
  post {
    failure {
      error 'Pipeline failed'
    }
  }
}
