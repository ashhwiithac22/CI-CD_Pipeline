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
                 sh 'echo "sdk.dir=/opt/Android/Sdk" > local.properties'
                       sh 'chmod -R 755 /opt/Android'
                       sh 'chmod +x gradlew'
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