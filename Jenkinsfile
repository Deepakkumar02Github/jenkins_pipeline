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
          def commandOutput = sh(script: 'test 5 -eq 15', returnStdout: true).trim()
          echo "$commandOutput"
        }
      }
    }
  }
}
