pipeline {
  agent {
    docker { image 'node:latest' }
  }
  stages {
    stage('setup'){
        steps{
            sh 'git config --global user.email "ujmore2407@gmail.com"'
            sh 'git config --global user.name "uj2407"'
        }
        
    }
    stage('Install') {
      steps { sh 'npm install' 
        echo 'Installation'
      }
    }
 
    stage('Test') {
      parallel {
        stage('Static code analysis') {
            steps { sh 'npm run-script lint' }
        }
        stage('Unit tests') {
            steps { sh 'npm run-script test' }
        }
      }
    }
 
    stage('Build') {
      steps { sh 'npm run-script build' }
    }
  }
}