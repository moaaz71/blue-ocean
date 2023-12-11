pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git 'https://github.com/moaaz71/moaaz.git'
      }
    }

    stage('build ') {
      steps {
        sh '''cd /var/lib/jenkins/workspace/blue-ocean_main
docker build -t java:v2 .
docker run -it -d -p 8080/9090 java-app2'''
      }
    }

  }
}