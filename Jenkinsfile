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

    stage('ssh') {
      steps {
        sshPublisher(masterNodeName: '10.29.42.141')
      }
    }

  }
}