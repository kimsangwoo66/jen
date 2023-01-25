pipeline {
  agent any
  stages {
    stage('git scm update') {
      steps {
        git url: 'https://github.com/kimsangwoo66/jen', branch: 'main'
      }
    }
    stage('docker build') {
      steps {
        sh '''
        mkdir /news
        '''
      }
    }
    
   
    
  }
}
