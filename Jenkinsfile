pipeline {
  agent {
    docker {
      image 'maven:3.6-jdk-8'
      args '-v $HOME/.m2:/root/.m2 -u 1003'
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
