pipeline {
  agent {
    docker {
      args '--user root'
      image 'turbobasic/gpp-alpine'
    }

  }
  stages {
    stage('Dependencies') {
      steps {
        sh 'printenv | sort'
        sh 'g++ --version'
      }
    }
    stage('Build') {
      steps {
        sh '''make
make install'''
      }
    }
    stage('Shared lib test') {
      steps {
        library 'bob-testing'
      }
    }
  }
}