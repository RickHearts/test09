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
          agent {
            node {
              label 'ubunto_slave1'
            }

          }
          steps {
            echo 'Mozilla Tests'
          }
        }

      }
    }

  }
}