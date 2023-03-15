pipeline {
	agent {
		label {
			label "built-in"
			customWorkspace "/mnt/httpd-1"
		}
	}
	stages {
		stage ("23Q1") {
			steps {
				sh "docker run -itdp 802:80 --name 23Q1 httpd"
				sh "docker cp /mnt/httpd-1/index.html 23Q2:/usr/local/apache2/htdocs"
				sh "docker exec 23Q1 chmod 777 /usr/local/apache2/htdocs/index.html"
			}
		}
	}
}
