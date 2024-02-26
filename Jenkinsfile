pipeline {
  agent any 

  tools {
    maven 'Maven3'
  }

  stages {
    stage ('scm-checkout') {
      steps {
        git changelog: false, poll: false, 
        url: 'https://github.com/ash2code/calculator-cicd.git'
      }
    }
    stage ('code-build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}
