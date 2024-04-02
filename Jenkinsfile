pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/tuanthanh201/maven-samples-A6', branch: 'master')
      }
    }
  }
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
}
