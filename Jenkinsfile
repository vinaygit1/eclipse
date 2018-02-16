pipeline {
  agent any
  stages {
    stage('SCM CheckOut') {
      steps {
        git(url: 'https://github.com/ranjeetgill/eclipse.git', branch: 'master')
      }
    }
  }
}