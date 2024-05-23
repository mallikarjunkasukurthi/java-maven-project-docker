pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
				sh "mvn --version"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration test"
			}
		}
	}
	post {
		always {
			echo "I am god . I run always"
		}
		success {
			echo "I run . whe it is success"
		}
		failure {
			echo "when it is failure"
		}
	}
}
