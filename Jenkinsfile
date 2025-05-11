pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        sh 'touch important_file.txt'
        sh 'echo Building the project... | tee -a important_file.txt'
        sh 'echo Project built! | tee -a important_file.txt'
      }
    }
    stage ('Test') {
      steps {
        script {
          // Capture and display the output
          def commandOutput = sh(script: 'test 5 -eq 5', returnStdout: true).trim()
          echo "$commandOutput"
        }
      }
    }
    stage ('Archive artifacts') {
      steps {
         archiveArtifacts artifacts: "important*", fingerprint: true
      }
     
    }
  }
}
