pipeline {
  agent any
  stages {
    stage('code checkout') {
      parallel {
        stage('code checkout') {
          steps {
            echo 'code checkout from SCM'
          }
        }

        stage('Test') {
          steps {
            echo 'Test execution'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }

  }
}