pipeline {
  agent any
  stages {
    stage('Code CheckOut') {
      steps {
        git(url: 'https://github.com/ranjeetgill/neweclipse.git', branch: 'master', poll: true)
      }
    }
    stage('Build Code') {
      steps {
        sh 'sh "\'/opt/apache-maven/bin/mvn\' -Dmaven.test.failure.ignore clean package"'
      }
    }
  }
}