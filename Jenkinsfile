pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Started build'
               // ng build
                echo 'Building'
            }
        }
        stage('Run'){
            steps{
                echo 'started run'
                npm run
                echo 'Running'
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