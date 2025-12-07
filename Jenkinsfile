pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/bishowessa/20226028_Bishoy_Maged_Makram_hosting.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install -g firebase-tools'
            }
        }
        //comment 2

        stage('Deploy to Firebase') {
            steps {
                bat 'firebase deploy --token "$FIREBASE_TOKEN" --non-interactive --only hosting'
            }
        }
    }
}