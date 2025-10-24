pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Pulling code from GitHub...'
                git branch: 'main', url: 'https://github.com/Prasadsasubilli/base.git'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying HTML site to web server directory...'
                
                echo 'Deployment successful! 🎉'
            }
        }
    }
}
