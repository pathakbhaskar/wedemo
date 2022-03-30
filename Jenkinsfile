pipeline {
  agent any
  stages {
    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Start Apache') {
      steps {
        sh 'sudo service apache2 start'
      }
    }

    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/pathakbhaskar/wedemo.git', branch: 'master')
      }
    }

    stage('Deploy Application') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}