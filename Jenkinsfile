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
        sudo docker build -t rapa.iptime.org:5000/nginx:1.0 .
        sudo docker push rapa.iptime.org:5000/nginx:1.0
        '''
      }
    }
    
    stage('deploy k8s') {
      steps {
        sh '''
        sudo kubectl apply -f test.yml
        '''
      }
    }
    
  }
}
