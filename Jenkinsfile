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
        retry(count: 3) {
          sh 'echo "Hello world"'
        }
        
      }
    }
  }
  environment {
    foo = 'bar'
  }
}