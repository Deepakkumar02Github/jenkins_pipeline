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
        sh 'test 5 -eq 5'
        sh 'test -f Jenkinsfile'
      }
    }
  }
}
