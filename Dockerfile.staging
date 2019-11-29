from alpine:3.9

run apk update && \
	apk add --no-cache \
	apache2 \
	php7-apache2 \	
	git

workdir /var/www/localhost/htdocs/

run git clone -b staging https://github.com/maximalyono/landing-page.git
run mv /var/www/localhost/htdocs/landing-page/* /var/www/localhost/htdocs/

run rm -rf /var/www/localhost/htdocs/landing-page

expose 80

cmd ["/usr/sbin/httpd", "-D", "FOREGROUND"]
