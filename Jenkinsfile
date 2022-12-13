pipeline {
  agent {
      docker {
          image 'gradle:6.6.1-jre14-openj9'
      }
  }
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