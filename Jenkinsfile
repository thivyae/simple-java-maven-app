pipeline {
  agent none
  stages {
    stage('Chekckout Frontend code And Run UnitTests') {
      parallel {
        stage('Chekckout App And Run UnitTests') {
          steps {
            echo '"Running unit tests"'
          }
        }

        stage('Checkout Backend Code And Run Unit tests') {
          steps {
            echo 'running unit tests'
          }
        }

      }
    }

    stage('Build and Package the frontend code') {
      parallel {
        stage('Build and Package the Frontend App') {
          steps {
            echo 'Building App'
          }
        }

        stage('Build Package BAckend') {
          steps {
            echo 'Building package'
          }
        }

      }
    }

    stage('Deploy Frontend and backend Packages To Env') {
      steps {
        echo 'Deploying UI and API code to an environemnt to test'
      }
    }

    stage('Run Functional tests') {
      parallel {
        stage('Run Functional tests') {
          steps {
            echo 'Running functional tests'
          }
        }

        stage('Run API tests') {
          steps {
            echo 'Running api test'
          }
        }

      }
    }

    stage('Deploy app to Prod') {
      steps {
        echo 'Deploying app to prod after all tests pass'
      }
    }

  }
}