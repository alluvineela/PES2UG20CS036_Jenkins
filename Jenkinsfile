pipeline {
    agent any
    stages {
        stage( 'Build') {
            steps {
                sh 'g++ pes2ug20cs036.cpp'
                echo 'Build Stage Successful '
            }
        }
        stage( 'Test') {
             steps {
                sh './pes2ug20cs036'
                echo 'Test Stage Successful '
             }
        }
        stage( 'Deploy') {
            steps {
                echo 'Deployment Successful '
            }
        }
    }
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
