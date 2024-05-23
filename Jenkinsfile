pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
				sh "mvn --version"
				echo "PAT - $PATH"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_URL - $env.BUILD_URL"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "JOB_NAME - $env.JOB_NAME"
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
