pipeline {
	agent any 
	stages {
		stage('cloning stage') {
			steps {
				checkout scm
			}
		}
		stage('building stage') {
			steps {
				sh 'mvn install'
			}
		}
		stage('deploying stage') {
			steps {
				sh 'scp target/flipkarts.war root@172.31.34.4:/root/source-test/apache-tomcat-10.1.61/webapps'
			} 
		}
	}
}
				
