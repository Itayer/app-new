pipeline {
  agent {
    node {
      label '34.76.66.41'
    }

  }
  stages {
    stage('resotre') {
      steps {
        sh 'npm install'
      }
    }
    stage('test') {
      steps {
        sh 'npm test'
      }
    }
    stage('build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('archive') {
      steps {
        archiveArtifacts '*.zip'
      }
    }
  }
}