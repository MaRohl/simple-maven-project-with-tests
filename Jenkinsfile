pipeline {
  agent {
    kubernetes {
      label BUILD_TAG
      containerTemplate {
        name 'maven'
        image 'maven'
        command 'sleep'
        args 'infinity'
      }
    }
  }
  stages {
    stage('Run') {
      steps {
        container('maven') {
          bat 'mvn -B -ntp -Dmaven.test.failure.ignore verify'
        }
      }
    }
  }
}
