pipeline {
  agent any

  stages {

      stage('Compile') {
        steps {
          echo 'Compile'
        }
      }

      stage('Test Cases') {
        when {
          expression { env.BRANCH_NAME != 'main' }
        }
        steps {
          echo 'Test Cases'
        }
      }

      stage('Docker Build') {
        when {
          not {
            branch '**'
          }
          tag ''
        }
        steps {
          echo 'Docker Build'
        }
      }

      stage('Docker Push') {
        when {
          not {
            branch '**'
          }
          tag ''
        }
        steps {
          echo 'Docker Push'
        }
      }

      stage('Deploy to Dev') {
        when {
          not {
            branch '**'
          }
          tag ''
        }
        steps {
          echo 'Deploy to Dev'
        }
      }

  }

}

