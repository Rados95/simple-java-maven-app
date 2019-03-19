pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:C:/Users/r.acimovic/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'hey'
            }
        }
    }
}