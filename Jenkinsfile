pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './gradlew build'
            }
            
        }
        stage('aving artifact') {
            steps {
                archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
            }
        }
    }
}
