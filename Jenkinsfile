pipeline {
  agent any
  stages {
    stage('Chrome') {
      steps {
        echo 'Chrome Test'
      }
    }

    stage('Firefox') {
      parallel {
        stage('Firefox') {
          steps {
            echo 'Firefox Tests'
          }
        }

        stage('Mozilla') {
          steps {
            echo 'Mozilla Tests'
          }
        }

      }
    }

  }
}