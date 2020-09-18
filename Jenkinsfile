pipeline {
	agent none
	stages {
		parallel{
		stage ('C Project') {
			agent { label 'node2' }
			steps {
			  	git 'https://github.com/Diwakar-Rajanna/c-project.git'
					sh 'make'
			}
		}
		stage ('Java Project') {
			agent { label 'node1' }
			steps {
				git 'https://github.com/Diwakar-Rajanna/java-project2.git'
				sh 'mvn clean install'
			}
		}
		}
	}
}
