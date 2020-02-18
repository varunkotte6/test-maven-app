pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'mvn package'
      }
    }

    stage('') {
      steps {
        archiveArtifacts 'C:\\Program Files (x86)\\Jenkins\\workspace\\test-maven-app_master\\target\\*'
      }
    }

  }
}