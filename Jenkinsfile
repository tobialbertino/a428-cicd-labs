node {
  agent {
    docker {
      image 'node:lts-bullseye-slim' 
      args '-p 3000:3000' 
    }
  }
  stage('Build') {
    sh 'npm install'
  }
  stage('Test') {
    steps {
      sh './jenkins/scripts/test.sh'       
    }
  }
}