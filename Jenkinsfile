pipeline {
  agent any
  stages {
    stage('test') {
	writeFile file: "application-test.sh", text: "echo Built ${BUILD_ID} of ${JOB_NAME}"
        archiveArtifacts artifacts: '*.sh', fingerprint: true
        echo 'test successful'
      }
    }
  }
}
