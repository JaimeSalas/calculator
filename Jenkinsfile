pipeline {
  agent any
  stages {
    stage('setup'){
      steps {
        dir("$WORKSPACE/calculator") {
          sh 'chmod +x gradlew'
        }
      }
    } 

    stage('Build'){
      steps {
        dir("$WORKSPACE/calculator") {
          sh './gradlew compileJava'
        }
      }
    }

    stage('Test'){
      steps {
        dir("$WORKSPACE/calculator") {
          sh './gradlew test'
        }
      }
    }
  }
}