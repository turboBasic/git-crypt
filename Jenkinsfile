pipeline {
  agent {
    docker {
      image 'phusion/baseimage'
    }

  }
  stages {
    stage('Dependencies') {
      steps {
        sh 'printenv | sort'
        sh '''apt update && apt upgrade --yes
apt install --yes make g++ libssl-dev'''
        sh 'g++ --version'
      }
    }
  }
}