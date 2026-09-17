pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                // Replace <student-username> and <repo-name> with your actual GitHub details
                git branch: 'Q2', url: 'https://github.com/Maddy19032006/ASS7.git'
            }
        }
        stage ('Generate Report') {
            steps {
                bat 'python app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
