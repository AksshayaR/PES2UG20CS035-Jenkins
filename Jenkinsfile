pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                 sh 'g++ hello.cpp -o hello'
                 build job: 'PES2UG20CS035-1', wait: false
                 echo 'Build by CS035 successful'
            }
        }

        stage('Test') {
            steps {
               sh 'cat hello.cpp'
                echo 'Test by CS035 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS035 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
