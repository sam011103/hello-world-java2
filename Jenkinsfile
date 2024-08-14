pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/nawaf83/hello-world-java1.git'
            }
        }
        stage('Build') {
            steps {
                powershell  'gradle build'
            }
        }
        stage('Test') {
            steps {
                powershell  'gradle test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'java -jar build/libs/hello-world-java-V1.jar'
            }
        }
    }
}
