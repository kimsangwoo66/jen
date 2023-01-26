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
        cd /ref
        sudo docker build -t 192.168.55.82:5000/nginx:k .
        '''
      }
    }
    
    stage('docker push') {
      steps {
        sh '''
        sudo docker push 192.168.55.82:5000/nginx:k
        '''
      }
    }
    
   
    
  }
}
