pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/prasannac-ai/hashapp-gr.git'
            }
        }

        stage('Clean') {
            steps {
                sh "/opt/gradle/bin/gradle clean"
            }
        }
        
        stage('Build') {
            steps {
                sh "/opt/gradle/bin/gradle build"
            }
        }
        
           stage('Test') {
            steps {
                sh "/opt/gradle/bin/gradle test"
            }
        }
        
          stage('Deploy') {
            steps {
                sh "/opt/gradle/bin/gradle run"
            }
        }

    }
}
