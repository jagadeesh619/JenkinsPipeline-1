pipeline {
    agent any
    environment {
        app="HPPV"
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