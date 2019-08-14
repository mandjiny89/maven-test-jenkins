pipeline {
    agent any
    stages {
        stage('clean') {
            steps {
                sh './clean'
            }
        }
        stage('compile') {
            steps {
                sh './compile'
            }
        }
        stage('package') {
            steps {
                sh './package'
            }
        }
                stage('Install') {
            steps {
                sh './install'
            }
        }
    }
}
