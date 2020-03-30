pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building or resolving dependencies!'
                sh 'bundle install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running regression tests!'
            }
        }
        stage('UAT') {
            steps {
                echo 'Wait for User Acceptance!'
                input(message: 'Go to production?', ok: 'Yes')
            }
        }
        stage('Prod') {
            steps {
                echo 'Webapp is Ready'
            }
        }
    }
}
