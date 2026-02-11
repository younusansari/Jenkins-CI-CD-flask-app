pipeline {
    agent any // Tells Jenkins where to run the pipeline
    stages {
        stage('checkout') {
            steps {
                echo 'Checking out the code from repository...'
            }
        }
 
        stage('install') {
            steps {
                echo 'Installing the application...'
            }
        }
 
        stage('build') { 
            steps {
                echo 'Building the application...'
            }
        }
    }
}