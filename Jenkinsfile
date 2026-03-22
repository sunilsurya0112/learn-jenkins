pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                sh 'sleep 10'
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
                //error 'pipeline failed'
            }
        }
    }
    post{
        always{
            echo "This seciton runs always"
            deleteDir()
        }
        success{
            echo "This section runs when pipeline is successs"
        }
        failure{
            echo "This section runs when pipeline failure"
        }
    }
}