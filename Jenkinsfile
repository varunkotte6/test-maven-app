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
        bat 'scp -r dist pdaus@10.29.42.141:/home/pdaus/'
      }
    }

  }
}