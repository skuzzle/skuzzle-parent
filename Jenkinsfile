pipeline {
  agent {
    docker {
      image 'maven:3.6-jdk-8'
      args '-v $HOME/.m2:/var/jenkins_home/.m2'
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
