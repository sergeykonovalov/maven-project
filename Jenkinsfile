pipeline {
  agent any
  tools {
    maven "M3"
  }
  stages {
    stage ('Build') {
      steps {
        sh "mvn clean package"
      }
      post {
        success {
          echo "Archiving..."
          archiveArtifacts artifacts: "**/target/*.war"
        }
      }
    }
  }
}
