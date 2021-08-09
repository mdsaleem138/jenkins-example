pipeline {
	agent {  label 'Linux node' }
	stages {
		stage('---clean---'){
			tools {
				maven 'MVN -3.81'
			}
			steps {
				
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'MVN 3.6.3'
			}
			steps {
				
				sh "mvn test"
			}
		}
		stage('---package---'){
			tools {
				maven 'MVN 3.6.2'
			}
			steps {
				
				sh "mvn package"
			}
		}
	}
	post {
		always {
			echo 'job was built successfully'
		}
	}
}
