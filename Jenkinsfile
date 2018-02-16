pipeline {
  agent any
  stages {
    stage('SCM CheckOut') {
      steps {
        git(url: 'https://github.com/ranjeetgill/eclipse.git', branch: 'master')
      }
    }
    stage('Build war') {
      steps {
        sh 'mvn clean install -f myapp/pom.xml'
      }
    }
    stage('Deploy2Tomcat') {
      steps {
        sh 'sudo cp myapp/target/myapp.war /opt/tomcat/webapps/'
      }
    }
  }
}