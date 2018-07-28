#!groovy

pipeline {
  agent none {
    stage('maven install'){
      agent {
        docker {
          image 'maven:3.5.0'
        }
      }
      steps {
        sh 'mvn clean install'
      }
    }
  }
}
