pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('checkout') {
			steps {
				echo "Build"
				sh "mvn --version"
				sh "docker --version"
				echo "PAT - $PATH"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_URL - $env.BUILD_URL"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "JOB_NAME - $env.JOB_NAME"
			}
		}
		stage('compile') {
			steps {
				sh "mvn clean compile"
			}
		}
		stage('Test') {
			steps {
				sh "mvn test"
			}
		}
		stage('Integration Test') {
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
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
