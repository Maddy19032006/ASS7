pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                // Replace <student-username> and <repo-name> with your actual GitHub details
                git branch: 'Q3', url: 'https://github.com/Maddy19032006/ASS7.git'
            }
        }
        stage ('Parallel Checks') {
            parallel {
                stage('Frontend Check') {
                    steps {
                        bat 'python frontend_check.py'
                    }
                }
                stage ('Backend Check') {
                    steps {
                        bat 'python backend_check.py'
                    }
                }
            }
        }
        stage('Summary') {
            steps {
                echo 'Both frontend and backend checks are complete.'
            }
        }
    }
}
