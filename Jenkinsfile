pipeline {
    agent { docker 'python:3.5.1' }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }

         stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }
        stage('test') {
            steps {
                sh 'echo "Test is working"'
            }
        }
         stage('deploy') {
            steps {
                sh 'echo "deploying..."'
            }
        }


    }
} 
