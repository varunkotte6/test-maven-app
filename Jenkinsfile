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
        powershell 'winscp -r target/* pdaus@10.29.42.46:/home/pdaus/jars/'
      }
    }

    stage('codessh') {
      steps {
        powershell 'scp -r src/* pdaus@10.29.42.46:/home/pdaus/code'
      }
    }

  }
}