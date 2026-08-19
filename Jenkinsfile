pipeline {
    agent any

    stages {
        stage('1. Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('2. Deploy to Apache') {
            steps {
                echo 'Deploying website files to Apache web root...'
                sh 'cp -rf * /var/www/html/'
            }
        }
    }

    post {
        success {
            echo 'Website deployed successfully!'
        }
        failure {
            echo 'Deployment failed.'
        }
    }
}
