pipeline {
    agent any
    tools {
        maven 'Maven 3.6.1'
        jdk 'java-1.8.0-openjdk-headless-1.8.0.222.b10-0.el7_6.x86_64'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn clean' 
            }
            post {
                success {
                    sh'test' 
                }
            }
        }
    }
}
