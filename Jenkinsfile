pipeline {
	agent none

	stages {
		stage ('C Project') {
			agent { label 'java' }
			steps {
			  	git 'https://github.com/Diwakar-Rajanna/c-project.git'
					sh 'make'
			}
		}
		stage ('Java Project') {
			agent { label 'java-1' }
			steps {
				git 'https://github.com/Diwakar-Rajanna/java-project2.git'
				sh 'mvn clean install'
			}
		}
		
	}
}
