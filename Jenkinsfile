pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh "tar cvfz helloworld.tar.gz app.js config.json package.json"
      }
    }
    stage('publish') {
      steps {
        sh "aws s3 cp helloworld.tar.gz s3://helloworld-code " 
      }
    }
  }
}
