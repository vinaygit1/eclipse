pipeline {
  agent any
  stages {
    stage('Code CheckOut') {
      parallel {
        stage('Code CheckOut') {
          steps {
            git(url: 'https://github.com/ranjeetgill/eclipse.git', branch: 'master')
          }
        }
        stage('SCM Message') {
          steps {
            echo 'Code CheckOut Completed'
          }
        }
      }
    }
    stage('Build war') {
      steps {
        sh 'mvn clean install -f myapp/pom.xml'
      }
    }
    stage('Deploy war') {
      steps {
        sh 'sudo cp myapp/target/myapp.war /usr/share/tomcat/webapps/'
      }
    }
    stage('Message') {
      steps {
        echo 'Deployment Completed Successful'
      }
    }
  }
}