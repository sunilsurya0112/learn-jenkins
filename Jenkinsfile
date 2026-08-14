pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo Building..'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploying....'
            }
        }
    }
    post{
        always{
            echo "This section runs always"
        }
        success{
            echo "This sections runs when piepeline is success"
        }
        failure{
            echo "This section runs when pipeline fails"
        }
    }
}