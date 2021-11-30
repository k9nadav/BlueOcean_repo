pipeline {
  agent any
  stages {
    stage('git Checkout') {
      steps {
        git(url: 'https://github.com/k9nadav/BlueOcean_repo.git', branch: 'main')
        echo ' successfully checked out from GitHub'
      }
    }

    stage('Compile') {
      steps {
        sh 'bash compile.sh'
        echo 'compiled successfully'
      }
    }

    stage('package') {
      steps {
        sh 'bash package.sh'
        echo 'packaged successfully'
      }
    }

    stage('Deploy') {
      steps {
        sh 'bash deploy.sh'
        echo 'deployed Succesfuly'
      }
    }

  }
}