pipeline {

    agent {
      node {
         label 'AGENT-1'
           }
         }
    environment { 
           Greeting = 'Hello Jenkins'
    }
//Build
    stages {
        stage('Build') {
            steps {
                echo "Building ..."
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
            }
        }
        stage('Deploy') {
            steps {
                sh """
                       echo "I Wrote Shell script"
                       env
                """
            }
        }
    }
//post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure{
            echo "this runs when pipeline is failed, generally used to send some alerts"
        }
        success{
             echo 'I will say hello when pipe line is success'
        }
    }
}