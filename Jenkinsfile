pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/playbuzz-localizor/translations.git', branch: 'master', changelog: true)
      }
    }
    stage('Build') {
      steps {
        echo 'Building'
        readFile 'README.md'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }
  }
}