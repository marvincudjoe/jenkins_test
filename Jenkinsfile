pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/marvincudjoe/ds-and-algorithms', branch: 'main')
      }
    }
    stage('Unit & Integration Tests') {
      steps {
        script {
          try {
            sh './gradlew clean test --no-daemon' //run a gradle task
            }
            finally {              
              junit '**/build/test-results/test/*.xml' //make the junit test results available in any case (success & failure)
            }
          }
      }
    }
  }
}