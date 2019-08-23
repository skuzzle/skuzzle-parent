pipeline {
  agent {
    docker {
      image 'maven:3.6-jdk-8'
      args '-u 1003:1003 -v $HOME/.m2:/var/maven/.m2 -e MAVEN_CONFIG=/var/maven/.m2 -e JAVA_OPTS=-Duser.home=/var/maven'
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
