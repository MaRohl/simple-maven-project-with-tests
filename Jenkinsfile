node ('master') {
  checkout scm
  stage('Build') {
    withMaven(maven: 'M3') {
      bat 'mvn -Dmaven.test.failure.ignore clean package'
    }
  }
}
