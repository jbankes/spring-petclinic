#!groovy

pipeline {
  agent none
  stages {
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
    stage('docker build'){
      agent any 
      steps {
        sh 'docker build -t jbankes/spring-petclinic:latest .'
      }
    }
  }
}
