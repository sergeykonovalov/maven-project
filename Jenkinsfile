pipeline {
  agent any
  tools {
    maven "Local Maven 3.5.2"
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
