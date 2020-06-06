node {
	def app
	
	stage('Clone repository') {
		checkout scm
	}

	stage('Build image') {
		app = docker.build('sergioqa/example-app')
<<<<<<< HEAD
	}

	stage('Test') {
		app.inside {
			sh 'npm test'
		}
=======
>>>>>>> aa1e1fde5184552fe0049e377381382ddd35424e
	}

	stage('Push image') {
		docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
			app.push('latest')
		}
	}
}
