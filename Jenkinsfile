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
    stage("Consolidate Results") {
      steps {
        input("Do you want to capture results?")
        junit '**/target/surefire-reports/TEST-*.xml'
        archive 'target/*.jar'
      }
    }
  }
}
