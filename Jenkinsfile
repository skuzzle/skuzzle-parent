pipeline {
  agent {
    docker {
      image 'maven:3.6-jdk-8'
      args '-u 1003:1003'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean deploy'
      }
    }
  }
}
