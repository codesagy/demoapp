pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/codesagy/demoapp'
            }
        }
        stage('Build') {
            steps {
                bat 'echo Hello from Build stage'
            }
        }
        stage('Archive Artifact') {
            steps {
                archiveArtifacts artifacts: '**/target/*.jar', allowEmptyArchive: true
            }
        }
    }
}
