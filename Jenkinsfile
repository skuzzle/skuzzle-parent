pipeline {
  agent {
    docker {
      image 'maven:3.6-jdk-8'
      args '-v $HOME/.m2:/var/maven/.m2 -e MAVEN_CONFIG=/var/maven/.m2'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'id'
        sh 'mvn -Duser.home=/var/maven clean deploy'
      }
    }
  }
}
