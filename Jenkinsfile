pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/tuanthanh201/maven-samples-A6', branch: 'master')
      }
    }

    stage('bisect') {
      steps {
        sh '''git bisect start
git bisect good 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5
git bisect bad 198644632661c67b6c32f59e9047c11a70685e15
git bisect run mvn clean test '''
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}