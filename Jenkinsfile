#!groovy
pipeline {
	agent none
  stages {
  	stage('Maven Install') {
    	agent {
      	docker {
        	image 'maven:3.8.7'
        }
      }
      steps {
      	sh 'mvn --settings ./.mvn/local-settings.xml clean install'
      }
    }
  }
}
