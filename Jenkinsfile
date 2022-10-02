pipeline {
    agent {
        docker {
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}

// node {
//   stage('Build') {
//      docker {
//       image 'node:lts-bullseye-slim' 
//       args '-p 3000:3000' 
//     }.inside {

//       sh 'npm install'       
//     }
//   }
//   stage('Test') {
//      docker {
//       image 'node:lts-bullseye-slim' 
//       args '-p 3000:3000' 
//     }.inside {

//       sh './jenkins/scripts/test.sh'       
//     }
//   }
// }