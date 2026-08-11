pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests... Pass!'
            }
        }

        stage('Package') {
            steps {
                // Windows Batch command replacing 'sh'
                bat 'echo Build executed on %DATE% %TIME% > build-info.txt'
            }
        }
    }

    post {
        success {
            echo 'Build successful! Ready for release.'
        }
    }
}