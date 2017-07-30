pipeline {
    agent { docker 'node:6.3' }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    stage('deploy') {
      steps {
        parallel(
          "deploy": {
            retry(count: 3) {
              sh 'echo "Hello world"'
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
