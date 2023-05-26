pipeline {
  agent any
  
  stages {
    stage('Checkout') {
      steps {
        // Checkout React application code from GitHub
        git 'https://github.com/Rohitkhapre/react_demo.git'
      }
    }
    
    stage('Install Dependencies') {
      steps {
        // Install Node.js dependencies using npm
        sh 'npm install'
      }
    }
    
    stage('Build') {
      steps {
        // Build  React application
        sh 'npm run build'
      }
    }
    
    stage('Archive Build Artifacts') {
      steps {
        // Archive the build artifacts
        archiveArtifacts 'build/**'
      }
    }
  }
}
