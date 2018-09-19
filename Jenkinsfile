pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'haii'
            sh '''mvn verify
mvn test
mvn package'''
          }
        }
        stage('ansible-server') {
          steps {
            node(label: 'ansible-server')
          }
        }
        stage('creating directory') {
          steps {
            sh 'mkdir /var/jenkins/ansible'
          }
        }
      }
    }
    stage('stagging') {
      steps {
        sh 'echo " this is stagging"'
      }
    }
  }
}