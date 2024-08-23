pipeline {
    agent any
    environment {
        app="HPPV"
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'SECONDS')
        disableConcurrentBuilds()
    }
    stages{
        stage('Build'){
            steps{
                echo "Building the code"
            }
        }
        stage('testing'){
            steps{
                echo "Testing the code"
                sleep 10
                
            }
        }
        stage('deploy'){
            steps{

                echo "Deployed the code in ${app} server"
            }
        }
    }
    post {

        success{
            echo " Your pipeline job is success"
        }
        failure{
            echo " Your pipeline job is failure"
        }
    }
}