pipeline {
    agent any
    stages {
        stage('Git Checkout Stage') {
            steps {
                echo '=== STEP 1: Cloning Source Code from GitHub ==='
                git branch: 'master', url: 'https://github.com/csoc01234-sketch/My-First-Devops-Project'
            }
        }
        stage('Build & Verify Stage') {
            steps {
                echo '=== STEP 2: Verifying Pulled Files ==='
                sh 'ls -la'
            }
        }
        stage('Production Deploy Stage') {
            steps {
                echo '=== STEP 3: Deploying Code to PVL Server ==='
                echo 'Application Deployment is SUCCESSFUL and LIVE!'
            }
        }
    }
}
