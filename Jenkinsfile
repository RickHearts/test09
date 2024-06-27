pipeline {
  agent any
  stages {
    stage('Chrome') {
      parallel {
        stage('Chrome') {
          steps {
            echo 'Chrome Test'
          }
        }

        stage('Firefox') {
          steps {
            echo 'Firefox tests'
          }
        }

      }
    }

    stage('Build 1 Test') {
      steps {
        sh 'echo "My file" > a.out'
        bat 'mvn package'
      }
    }

    stage('Deploy') {
      steps {
        pwd(tmp: true)
        git 'https://github.com/RickHearts/mvn1'
      }
    }

  }
}