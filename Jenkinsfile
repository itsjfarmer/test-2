pipeline {
  agent any
  triggers { pollSCM('* * * * *') }
  stages {
    stage('test') {
	steps {
	writeFile file: "application-test.sh", text: "echo Built ${BUILD_ID} of ${JOB_NAME}"
        archiveArtifacts artifacts: '*.sh', fingerprint: true
        echo 'test successful'
	}
      }
    }
  }
