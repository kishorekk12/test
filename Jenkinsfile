pipeline {
  agent any
  stages {
    stage('code checkout') {
      parallel {
        stage('code checkout') {
          steps {
            git 'https://github.com/kishorekk12/pipelineTest.git'
          }
        }

        stage('Test') {
          steps {
           bat 'mvn install'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        deploy adapters: [tomcat8(credentialsId: '0547a943-3f60-4310-915f-bcb0ffe0b38c', path: '', url: 'http://localhost:8082/')], contextPath: null, war: '*/*.war'
      }
    }

  }
}
