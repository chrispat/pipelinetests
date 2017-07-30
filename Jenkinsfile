pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Hello World'
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