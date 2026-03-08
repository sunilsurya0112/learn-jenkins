pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
            }
        }
        stage('Test') {
            steps {
               sh 'echo This is test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is deploy'
                error 'pipeline failed'
            }
        }
    }
    post{
        always{
            echo "This seciton runs always"
        }
        success{
            echo "This section runs when pipeline is successs"
        }
        failure{
            echo "This section runs when pipeline failure"
        }
    }
}