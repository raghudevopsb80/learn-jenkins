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
        when {
          expression { env.BRANCH_NAME != 'master' }
        }
        steps {
          echo 'Test Cases'
        }
      }

      stage('Docker Build') {
        when {
          expression { env.BRANCH_NAME != 'master' }
        }
        steps {
          echo 'Docker Build'
        }
      }

      stage('Docker Push') {
        when {
          expression { env.BRANCH_NAME != 'master' }
        }
        steps {
          echo 'Docker Push'
        }
      }

      stage('Deploy to Dev') {
        when {
          expression { env.BRANCH_NAME != 'master' }
        }
        steps {
          echo 'Deploy to Dev'
        }
      }

  }

}

