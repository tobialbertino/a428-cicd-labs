node {
  agent {
    docker {
      image 'node:lts-bullseye-slim' 
      args '-p 3000:3000' 
    }
  }
  stage('Build') {
    docker.image('node:lts-bullseye-slim').inside {
            sh 'npm i'
        }
  }
  stage('Test') {
    steps {
      sh './jenkins/scripts/test.sh'       
    }
  }
}