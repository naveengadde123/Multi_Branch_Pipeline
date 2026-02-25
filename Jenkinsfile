pipeline {
    agent any

    stages {

        stage('Checkout Info') {
            steps {
                echo "Running Multibranch Pipeline"
                echo "Branch Name: ${env.BRANCH_NAME}"
            }
        }

        stage('Build') {
            steps {
                echo "Building application..."
            }
        }

        stage('Deploy to Dev') {
            when {
                branch 'develop'
            }
            steps {
                echo "Deploying to DEV environment"
            }
        }

        stage('Deploy to Production') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying to PRODUCTION environment"
            }
        }
    }
}