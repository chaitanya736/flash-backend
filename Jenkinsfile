pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        script {
          // Explicit branch + public repo handling
          git branch: 'main',
              url: 'https://github.com/chaitanya736/flash-backend.git'
        }
      }
    }
    

    stage('Restart Flask') {
      steps {
        sh 'pm2 restart flask-backend || pm2 start app.py --name flask-backend --interpreter python3'
      }
    }
  }
}
