pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        sh 'mvn install'
      }
    }
    stage ('Build the docker image') {
      steps {
        sh 'docker build -t mniligiri/firstrepo:v10 .'
        sh 'docker images'
      }
    }
    stage ('Push the docker image') {
      steps {
        sh 'docker push mniligiri/firstrepo:v10'
        }
    }
  }
}
