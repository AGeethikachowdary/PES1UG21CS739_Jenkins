pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // build 'PES1UG21CS739-1'
                sh 'g++ -o output main.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './out'
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
            echo 'Pipeline failed.'
        }
    }
}
