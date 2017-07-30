pipeline {
    agent { docker 'node:6.3' }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    stage('deploy') {
      agent { docker 'maven:3.3.3' }
      steps {
        parallel(
          "deploy": {
            retry(count: 3) {
              sh 'mvn --version'
            }
            
            
          },
          "deploy 2": {
            echo 'run deploy 2'
            
          }
        )
      }
    }
  }
  environment {
    foo = 'bar'
  }
}
