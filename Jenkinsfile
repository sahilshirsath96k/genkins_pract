pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'echo Checking out the code'
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                sh 'echo App is Building'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Tesing the Build'
            }
        }
        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                sh 'echo deploying the Build'
            }
        }
    }
    post {
        always {
            sh 'echo this always run'
        }
        success {
            sh 'echo successfully run'
            
        }
        failure {
            sh 'echo failed '
        }
    }
}
