pipeline {
    agent any
    
    // This tells Jenkins to keep the server clean
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out code from: ${env.GIT_URL}"
            }
        }
        stage('Build') {
            steps {
                echo "Building branch: ${env.BRANCH_NAME}"
                sh 'echo "Hello World" > build.txt'
            }
        }
    }
}
