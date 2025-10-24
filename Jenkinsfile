pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Pulling code from GitHub...'
                git branch: 'main', url: 'https://github.com/<your-username>/simple-html-site.git'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying HTML site to web server directory...'
                sh '''
                    sudo rm -rf /var/www/html/*
                    sudo cp -r * /var/www/html/
                '''
                echo 'Deployment successful! 🎉'
            }
        }
    }
}
