pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/ashhwiithac22/CI-CD_Pipeline.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew clean assembleDebug'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
        stage('Archive APK') {
            steps {
                archiveArtifacts artifacts: '**/build/outputs/apk/**/*.apk', fingerprint: true
            }
        }
    }
}