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
        stage('Test') {
            steps {
                sh 'echo "Test works"'
            }
        }
    }
 

post {
    always {
        archive 'build/libs/**/*.jar'
        junit 'build/reports/**/*.xml'
    }
}
}
