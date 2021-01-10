pipeline {
    agent  { docker { image 'python:3.5.1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'python printTest.py'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
