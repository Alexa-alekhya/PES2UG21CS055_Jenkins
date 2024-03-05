pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES2UG21CS055-1'
                    sh 'task5.cpp -o output'
                }
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
