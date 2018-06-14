pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        step([$class: 'CopyArtifact', projectName: 'application-build'])
        archiveArtifacts artifacts: '*.sh', fingerprint: true
        echo 'test successful'
      }
    }
  }
}
