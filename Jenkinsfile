pipeline {
  agent any
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
