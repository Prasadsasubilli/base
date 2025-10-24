pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Cloning repository from GitHub...'
                git branch: 'main', url: 'https://github.com/Prasadsasubilli/base.git'
            }
        }

        stage('Deploy to Web Server') {
            steps {
                echo 'Deploying HTML files to web server...'
                // Copy your HTML and CSS files to web directory
                sh '''
                sudo rm -rf /var/www/html/*
                sudo cp -r * /var/www/html/
                '''
            }
        }
    }

    post {
        success {
            echo '✅ Deployment successful! Website is live.'
        }
        failure {
            echo '❌ Deployment failed. Check Jenkins logs.'
        }
    }
}
