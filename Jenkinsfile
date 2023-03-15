pipeline {
	agent {
		label {
			label "built-in"
			customWorkspace "/mnt/httpd-2"
		}
	}
	stages {
		stage ("23Q2") {
			steps {
				sh "docker run -itdp 801:80 --name 23Q2 httpd"
				sh "docker cp /mnt/httpd-2/index.html 23Q2:/usr/local/apache2/htdocs"
				sh "docker exec 23Q2 chmod 777 /usr/local/apache2/htdocs/index.html"
			}
		}
	}
}
