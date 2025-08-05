pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        // For example, build a Docker image if you have Dockerfile
        // sh 'docker build -t myapp .'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        // Add commands to run app tests, e.g., running pytest
        // sh 'pytest tests/'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
        // For demo, you could run the app or deploy Docker container
        // sh 'docker run -d -p 5000:5000 myapp'
      }
    }
  }
}

