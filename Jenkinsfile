pipeline {
    agent any
    stages {
         stage('Clone repository') {
             steps {
                 checkout([$class: 'GitSCM',
                 branches: [[name: '*/main']],
                 userRemoteConfigs: [[url: 'https://github.com/SamrudhGShetty/PES1UG22AM146_Jenkins.git']]])
             }
         }

        stage('Build') {
            steps {
                build 'PES1UG22AM146-1'
                sh 'g++ main.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh 'input'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
   
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
