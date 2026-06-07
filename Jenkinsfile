pipeline {
    agent any
    
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['QA', 'Staging', 'Production'], description: 'Select the target server for deployment')
    }

    environment {
        COMPANY_NAME = 'PVL Creative Ad Agency'
    }

    stages {
        stage('Checkout & Verify') {
            steps {
                echo "=== Running Job for ${env.COMPANY_NAME} ==="
                git branch: 'master', url: 'https://github.com/csoc01234-sketch/My-First-Devops-Project'
                sh 'ls -la'
            }
        }
        
        stage('Dynamic Deployment') {
            steps {
                echo "=== Deploying Application to ${params.ENVIRONMENT} Server ==="
                echo "Deployment to ${params.ENVIRONMENT} environment is SUCCESSFUL!"
            }
        }
    }
}
