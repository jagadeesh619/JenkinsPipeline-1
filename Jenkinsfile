pipeline {
    agent any
    environment {
        app="HPPV"
    }
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['PROD', 'DEV', 'QA'], description: 'Pick which environment')
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }
    stages{
        stage('Build'){
            steps{
                echo "Building the code  in ${params.ENVIRONMENT}"
            }
        }
        stage('testing'){
            steps{
                echo "Testing the  code ${params.ENVIRONMENT}"                
            }
        }
        stage('deploy'){
            steps{

                echo "Deployed the code in ${params.ENVIRONMENT} ${app} server"
            }
        }
    }
    post {

        success{
            echo " Your pipeline job is success in environment ${params.ENVIRONMENT}"
        }
        failure{
            echo " Your pipeline job is failure in environment ${params.ENVIRONMENT}"
        }
    }
}