node() {

  sh 'env'

  if (env.TAG_NAME) {
    stage('Docker Build') {
      print 'Docker Build'
    }

    stage('Docker Push') {
      print 'Docker Push'
    }

    stage('Deploy to Dev') {
      print 'Deploy to Dev'
    }
  }
  else {
    stage('Compile') {
      print 'Compile'
    }

    stage('Test Cases') {
      print 'Test Cases'
    }
  }

}
