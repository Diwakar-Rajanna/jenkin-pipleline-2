pipeline {
	agent none
	stages {
		stage ('parallel '){
			parallel{
			stage ('C Project') {
				agent { label 'node2' }
				steps {
				  	git 'https://github.com/Diwakar-Rajanna/c-project.git'
						sh 'make'
					sleep 10
				}
			}
			stage ('Java Project') {
				agent { label 'node1' }
				steps {
					git 'https://github.com/Diwakar-Rajanna/java-project2.git'
					sh 'mvn clean install'
					sleep 10
				}
			}
		}
	}
}
}
