pipeline {
  agent any
  stages {
    stage('Get Checkout') {
      steps {
        git(url: 'https://github.com/k9nadav/BlueOcean_repo.git', branch: 'main')
        echo 'Successfully from GitHub '
      }
    }

    stage('Compile') {
      steps {
        sh 'bash compile.sh'
        echo 'Compiled'
      }
    }

    stage('package') {
      steps {
        sh 'bash package.sh'
        echo 'Packaged'
      }
    }

    stage('Deploy') {
      steps {
        sh 'bash deploy.sh'
        echo 'Deployed'
      }
    }

  }
}