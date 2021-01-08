pipeline {
  agent any
  stages {
    stage("Cleaning Stage") {
      steps {
        sh "/var/jenkins_home/maven/bin/mvn clean"
      }
    }
    stage("Testing Stage") {
      steps {
        sh "/var/jenkins_home/maven/bin/mvn test"
      }
    }
    stage("Packaging Stage") {
      steps {
        sh "/var/jenkins_home/maven/bin/mvn package"
      }
    }
  
  }
}
