pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/sam011103/hello-world-java2.git'
            }
        }

        
        stage('Build') {
            steps {

                        powershell 'gradle clean build'
                
            }
        }
        stage('Test') {
            steps {
                
                        powershell 'gradle test'
                  
            }
        }
        stage('Deploy') {
            steps {                
                        powershell 'java -jar build/libs/hello-world-java-V1.jar'
                 }           
        }
    
}

post {
       
        success {
            echo 'Build succeeded!!'
            // You could add notification steps here, e.g., send an email
        }
        failure {
            echo 'Build failed!1!'
            // You could add notification steps here, e.g., send an email or Slack message
        }
    }
    }


