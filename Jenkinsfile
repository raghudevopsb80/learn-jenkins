pipeline {
  agent any

  stages {

      stage('Compile') {
        when { branch 'main' }
        steps {
          echo 'Compile'
        }
      }

      stage('Test Cases') {
        expression { env.BRANCH_NAME != 'main' }
        steps {
          echo 'Test Cases'
        }
      }

      stage('Docker Build') {
        expression { env.BRANCH_NAME != 'main' }
        steps {
          echo 'Docker Build'
        }
      }

      stage('Docker Push') {
        expression { env.BRANCH_NAME != 'main' }
        steps {
          echo 'Docker Push'
        }
      }

      stage('Deploy to Dev') {
        expression { env.BRANCH_NAME != 'main' }
        steps {
          echo 'Deploy to Dev'
        }
      }

  }

}

