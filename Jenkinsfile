pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        step([$class: 'CopyArtifact', projectName: 'test-2'])
        archiveArtifacts artifacts: '*.sh', fingerprint: true
        echo 'test successful'
      }
    }
  }
}
