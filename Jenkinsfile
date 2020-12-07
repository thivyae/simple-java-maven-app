pipeline {
  agent none
  stages {
    stage('Chekckout App And Run UnitTests') {
      parallel {
        stage('Chekckout App And Run UnitTests') {
          steps {
            echo '"Running unit tests"'
          }
        }

        stage('Checkout Code And Run Unit tests') {
          steps {
            echo 'running unit tests'
          }
        }

      }
    }

    stage('Build and Package the App') {
      parallel {
        stage('Build and Package the App') {
          steps {
            echo 'Building App'
          }
        }

        stage('Build Package') {
          steps {
            echo 'Building package'
          }
        }

      }
    }

    stage('Deploy Packages To Env') {
      steps {
        echo 'Deploying UI and API code to an environemnt to test'
      }
    }

    stage('Run Functional tests') {
      steps {
        echo 'Running functional tests'
      }
    }

    stage('Deploy app to Prod') {
      steps {
        echo 'Deploying app to prod after all tests pass'
      }
    }

  }
}