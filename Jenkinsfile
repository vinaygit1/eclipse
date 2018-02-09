pipeline {
  agent any
  stages {
    stage('Code CheckOut') {
      steps {
        git(url: 'https://github.com/ranjeetgill/eclipse.git', branch: 'master')
      }
    }
    stage('Build war') {
      steps {
        sh 'mvn clean install -f myapp/pom.xml'
      }
    }
  }
}