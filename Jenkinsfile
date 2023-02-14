pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o task5_644.cpp task5_644.cpp'
                build job: 'PES1UG20CS644-1'
            }
        }

        stage('Test') {
            steps {
                sh './task5_644'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
