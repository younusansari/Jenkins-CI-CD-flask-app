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
                echo 'Deploying to Staging Environment...'
                sh '''
                python3 app.py &
                sleep 5 
                curl http://localhost:5000/
                '''

        }
    }
}