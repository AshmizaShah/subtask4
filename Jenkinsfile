
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the repository
                checkout scm
            }
        }

        stage('Run Tests') {
            steps {
                // Run the unit tests
                sh 'python -m unittest discover -v'
            }
        }
    }

    post {
        always {
            // Archive test reports
            junit 'reports/**/*.xml'
        }
    }
}