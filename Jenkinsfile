pipeline {
    agent none
    stages {
        stage('build') {
            agent { docker 'node:6.3' }
            steps {
                sh 'npm --version'
            }
        }
        stage('deploy') {
            agent { docker 'maven:3.3.3' }
            steps {
                sh 'mvn --version'
            }
        }
    }
  environment {
    foo = 'bar'
  }
}
