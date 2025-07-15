pipeline {
    agent any

    environment {
        BUILD_DIR = 'build'
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Example build step (adjust based on your tech stack)
                // For a Java app, you might run: sh 'mvn clean install'
            }
        }

        stage('Archive Artifact') {
            steps {
                echo 'Archiving build artifacts...'
                archiveArtifacts artifacts: "${BUILD_DIR}/**", allowEmptyArchive: true
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
