pipeline{
agent any
stages {
	stage('copy-index'){
		steps {
		sh 'chmod -R 777 index.html'
		sh 'cp -r index.html /var/www/html'
	}
	}
		stage('copy-dev'){
		steps {
		sh 'chmod -R 777 dev.html'
		sh 'cp -r dev.html /var/www/html'
	}
	}
		stage('copy-qa'){
		steps {
		sh 'chmod -R 777 qa.html'
		sh 'cp -r qa.html /var/www/html'
	}
	}
		stage('restart-httpd'){
		steps {
		sh 'service httpd start'
	}
	}
}
}
