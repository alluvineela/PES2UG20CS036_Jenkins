pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        // Perform build steps here
        sh 'mvn clean package'
      }
    }
    stage('Test') {
      steps {
        // Perform test steps here
        sh 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        // Perform deploy steps here
        sh 'scp target/myapp.war user@remote:/opt/tomcat/webapps'
      }
    }
  }
  post {
    always {
      echo 'Pipeline completed'
    }
    failure {
      echo 'Pipeline failed'
    }
  }
}
