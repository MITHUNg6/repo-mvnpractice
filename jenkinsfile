pipeline {
	agent any
	stages {
		stage('---clean---'){
			steps {
				tool name: 'maven3.3.9', type: 'maven'
				sh "mvn clean compile"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'maven3.5.3', type: 'maven'
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'maven3.3.3', type: 'maven'
				sh "mvn package"
			}
		}
	}
}
