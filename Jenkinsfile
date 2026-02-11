pipeline {
    agent any // Tells Jenkins where to run the pipeline
    stages {
        stage('build') {
            steps {
                echo 'Creating virtual environment and installing dependencies...'
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install -r Requirements.txt
                    python3 --version
                    pip3 --version
                    pytest --version
                '''
            }
        }
 
        stage('Testing') {
            steps {
                echo 'Running Unit Tests...'
                sh '''
                    . venv/bin/activate
                    pytest
                '''
            }
        }
 
        stage('deploy') { 
            steps {
                echo 'Building the application...'
            }
        }
    }
}