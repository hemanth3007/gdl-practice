pipeline {
	agents any
	tools {
		gradle 'gradle'
		jdk 'jdk'
	}
	stages {
		stage('Checkout') {
			steps {
				git branch: 'main', url: 'https://github.com/hemanth3007/gdl-practice.git'
			}
		}
		stage('Build') {
			steps {
				sh 'gradle build'
			}
		}
		stage('Test') {
			steps {
				sh 'gradle test'
			}
		}
		stage('Run Application') {
			steps {
				sh 'gradle run'
			}
		}
	}
	posts {
		success {
			echo 'Build and Deployment successful'
		}
		failure {
			echo 'Build Failed'
		}
	}
}
