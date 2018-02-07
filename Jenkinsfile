pipeline {
  agent any
  stages {
    stage('SCM CheckOut') {
      steps {
        git(url: 'git@github.com:ranjeetgill/neweclipse.git', branch: '/master')
      }
    }
  }
}