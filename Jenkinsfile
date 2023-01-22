#!groovy
pipeline {
	agent none
  stages {
  	stage('Maven Install') {
    	agent {
      	docker {
        	image 'maven:3.5.0'
        }
      }
      steps {
        sh 'rm -rf /var/jenkins_home/workspace/Spring-Petclinic/?/.m2/repository'
      	sh 'mvn -X clean install'
      }
    }
  }
}
