pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
         'mvn clean'
      }
    }
    stage('Test') {
      steps {
        'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        'mvn package'
      }
    }
    stage('report') {
      steps {
        cucumber fileIncludePattern: '**/*.json', sortingMethod: 'ALPHABETICAL'
      }
    }
  }
}
