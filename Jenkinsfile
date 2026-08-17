pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds()
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo Building..'
                //sh 'sleep 10'
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
            deleteDir()
        }
        success{
            echo "This sections runs when piepeline is success"
        }
        failure{
            echo "This section runs when pipeline fails"
        }
    }
}