pipeline {
  agent any
  
  stages {
    stage('Checkout') {
      steps {
        // Checkout your React application code from GitHub
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
        // Build your React application
        sh 'npm run build'
      }
    }
    
    stage('Archive Build Artifacts') {
      steps {
        // Archive the build artifacts (e.g., build output files)
        archiveArtifacts 'build/**'
      }
    }
  }
}
