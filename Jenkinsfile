node {
  stage('Build') {
     docker {
      image 'node:lts-bullseye-slim' 
      args '-p 3000:3000' 
    }
    
        sh 'npm install'       
  }
  stage('Test') {
     docker {
      image 'node:lts-bullseye-slim' 
      args '-p 3000:3000' 
    }
       
  }
}
