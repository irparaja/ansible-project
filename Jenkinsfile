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
      parallel {
        stage('stagging') {
          steps {
            sh 'echo " this is stagging"'
          }
        }
        stage('testing') {
          steps {
            emailext(subject: 'this is for testing phase', body: 'nayanatara body ', from: 'irparajabab5190@gmail.com', replyTo: 'irparajabab5190@gmai.lcom', to: 'irparajababu5190@gmail.com')
          }
        }
      }
    }
  }
}