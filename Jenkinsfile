pipeline {
  agent any
  stages {
    stage('Say Hello') {
      parallel {
        stage('Say Hello') {
          steps {
            sh '''echo "Hello World"
'''
          }
        }

        stage('build-App') {
          agent {
            docker {
              image 'gradle:6.8.3-jdk11'
            }

          }
          steps {
            sh '''

ci/build-app.sh'''
          }
        }

        stage('') {
          steps {
            sh 'chmod 755 ci/build-app.sh'
          }
        }

      }
    }

  }
}