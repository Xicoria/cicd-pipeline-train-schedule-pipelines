pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building project..."
                sh './gradlew build --no-daemon'
            }
            
        }
        stage('Saving artifact') {
            steps {
                echo "Archiving build..."
                archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
            }
        }
    }
}
