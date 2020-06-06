node {
	def app
	
	stage('Clone repository') {
		checkout scm
	}

	stage('Build image') {
		app = docker.build('mjuuso/example-app')
	}

	stage('Push image') {
		docker.withRegistry('https://registry.hib.docker.com', 'docker-hub-credentials') {
			app.push('latest')
		}
	}
}
