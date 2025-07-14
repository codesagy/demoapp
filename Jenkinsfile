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
                sh 'mvn clean package'
            }
        }

        stage('Archive Artifact') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }

    post {
        success {
            echo '✅ Build and archive successful!'
        }
    }
}
