pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
				 bat 'mvn -B -DskipTests clean package'
			}
		}
		stage('Test') {
			steps {
				 bat 'mvn test'
			}
		}
		stage('Dir') {
			steps {
				 bat ' dir /S target'
			}
		}
		
		stage('Jenkins'){
			bat 'mvn jenkins:deploy tomcat'
		
		}
	}
}
