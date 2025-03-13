pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                build "PES2UG22CS213-CCLAB"
                sh 'g++ main/hello.cpp -o output'

            }
        }
        
        stage('Test') {
            steps {
                sh './output'
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
            echo 'Pipeline failed'
        }
    }
}
