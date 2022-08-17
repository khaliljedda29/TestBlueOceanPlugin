pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
        retry(count: 3) {
          sh 'hhhhh'
        }

      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are u sure to deploy ?', ok: 'yes')
        echo 'Deployement completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New build completed successufelly'
      }
    }

  }
}