pipeline {
    agent any

    stages {
        stage('Check Python Version') {
            steps {
                sh '/usr/bin/python3.9 --version'
            }
        }

        stage('Run Python Tests') {
            steps {
                sh '/usr/bin/python3.9 -m unittest discover -v'
            }
        }
    }
}
