pipeline {
  agent {label 'test_node'}
  stages {
    stage ('Build') {
      steps {
        sh 'echo "Building the project"'
      }
    }
    stage ('Test') {
      steps {
        script {
          // Capture and display the output
          def commandOutput = sh(script: 'echo hello', returnStdout: true).trim()
          echo "$commandOutput"
        }
      }
    }
  }
}
