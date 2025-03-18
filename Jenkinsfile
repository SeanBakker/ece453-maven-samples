pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/SeanBakker/ece453-maven-samples.git', branch: 'master')
      }
    }

    stage('run') {
      agent any
      steps {
        sh 'mvn clean'
        sh 'mvn test'
        sh 'mvn verify'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
  environment {
    DHT_SENSE = 'C:\\Users\\sbakk\\.jdks\\jbr-17.0.12'
    DHT_MVN = '3.9.7'
  }
}