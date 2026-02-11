pipeline {
    agent any // Tells Jenkins where to run the pipeline
    stages {
        stage('build') {
            steps {
                echo 'Checking out the code from repository...'
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install -r Requirements.txt
                '''
            }
        }
 
        stage('install') {
            steps {
                echo 'Installing the application...'
            }
        }
 
        stage('deploy') { 
            steps {
                echo 'Building the application...'
            }
        }
    }
}