pipeline {
  agent any
  stages {
    stage('setup'){
      steps {
        sh 'ls -al'
        sh 'echo $WORKSPACE'
        sh 'chmod +x gradlew'
      }
    } 

    stage('Build'){
      steps {
        sh './gradlew compileJava'
      }
    }

    stage('Test'){
      steps {
        sh './gradlew test'
      }
    }
  }
}