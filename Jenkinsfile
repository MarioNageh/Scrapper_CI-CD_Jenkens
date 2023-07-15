pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/MarioNageh/Scrapper_CI-CD_Jenkens', branch: 'main')
      }
    }

    stage('Build Docker') {
      steps {
        sh '''docker build -t scrapper_jen .
docker run -p 8085:8000 scrapper_jen'''
      }
    }

  }
}