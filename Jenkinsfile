pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                ng build
            }
        }
        stage('Run'){
            steps{
                ng serve
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