pipeline {
  agent any
  stages {
    stage('Initializing') {
      parallel {
        stage('SCM Checkout') {
          steps {
            echo 'SCM checkout'
          }
        }
        stage('build-1') {
          steps {
            echo 'build code'
          }
        }
        stage('build-2') {
          steps {
            echo 'building code 2'
          }
        }
      }
    }
    stage('Testing') {
      steps {
        echo 'Jnuit testing'
      }
    }
    stage('Artifactory') {
      steps {
        echo 'Uploading to nexus'
      }
    }
    stage('Cleanup') {
      steps {
        echo 'cleaning everything'
      }
    }
  }
}
