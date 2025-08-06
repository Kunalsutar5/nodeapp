pipeline {
  agent any
  tools { nodejs 'node18' }
  stages {
    stage('Checkout') { steps { git url: 'https://github.com/Kunalsutar5/nodeapp.git', branch: 'main' } }
    stage('Install') { steps { sh 'npm install' } }
    stage('Test') { steps { sh 'npm test || true' } }
    stage('Build') { steps { sh 'npm run build || echo "no build"' } }
    stage('Deploy') { steps { sh './deploy.sh' } }
  }
}
