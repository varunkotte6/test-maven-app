pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'mvn package'
      }
    }

    stage('error') {
      steps {
        archiveArtifacts 'target\\*'
      }
    }

  }
}