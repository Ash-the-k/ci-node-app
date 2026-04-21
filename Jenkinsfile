pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Application') {
            steps {
                sh 'node app.js'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'node test'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline Success'
        }
        failure {
            echo 'CI Pipeline Failed!'
        }
    }
}