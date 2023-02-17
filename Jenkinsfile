pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                 sh 'g++ error.cpp -o error'
                 build job: 'PES2UG20CS036-1', wait: false
                 echo 'Build by CS036 successful'
            }
        }

        stage('Test') {
            steps {
               sh 'cat pes2ug20cs036.cpp'
                echo 'Test by CS036 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS036 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
