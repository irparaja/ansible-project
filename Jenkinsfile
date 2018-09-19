pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'haii'
        sh '''mvn verify
mvn test
mvn package'''
      }
    }
    stage('stagging') {
      steps {
        sh 'echo " this is stagging"'
      }
    }
  }
}