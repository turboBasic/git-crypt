pipeline {
  agent {
    docker {
      image 'phusion/baseimage'
      args '--user root'
    }

  }
  stages {
    stage('Dependencies') {
      steps {
        sh 'printenv | sort'
        sh '''apt update
apt install --yes make g++ libssl-dev'''
        sh 'g++ --version'
      }
    }
  }
}