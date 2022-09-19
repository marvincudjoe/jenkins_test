pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/marvincudjoe/ds-and-algorithms', branch: 'main')
      }
    }

    stage('') {
      steps {
        withGradle() {
          sh './gradlew test'
        }

      }
    }

  }
}