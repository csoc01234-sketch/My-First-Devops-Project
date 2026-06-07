pipeline {
    // ఇక్కడ మనం జెంకిన్స్ కి చెప్తున్నాం: "ఈ జాబ్ ని మాస్టర్ లో కాకుండా PVL-Linux-Agent లోనే రన్ చెయ్" అని
    agent { label 'PVL-Linux-Agent' }
    
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['QA', 'Staging', 'Production'], description: 'Select the target server for deployment')
    }

    environment {
        COMPANY_NAME = 'PVL Creative Ad Agency'
    }

    stages {
        stage('Checkout & Verify') {
            steps {
                echo "=== Running Job on Dedicated Agent for ${env.COMPANY_NAME} ==="
                git branch: 'master', url: 'https://github.com/csoc01234-sketch/My-First-Devops-Project'
                sh 'ls -la'
            }
        }
    }
}
