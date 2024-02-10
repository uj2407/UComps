	
pipeline {
  agent {
    docker { image 'node:latest',
        docker build . --pull
    }
  }
  stages {
    stage('Install') {
      steps { sh 'npm install' }
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