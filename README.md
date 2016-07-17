# Docker Notes

### Download docker:
	docker pull php:5.6-apache

### run docker with container name "app1" mapping machine port 80 container port 80
	docker run --name app1 -d -p 80:80 -it -v "$PWD":/var/www/html php:5.6-apache

### List running docker
	docker ps

### Remove container name "app1"
	docker rm -f app1

### Build new docker from Dockerfile with name "app1:php-5.6", note last dot in command
	docker build -t app1:php-5.6 .

### Save docker to tar file
	docker save app1:php-5.6 > ~/app1-php-56.tar

### Docker Compose
	“Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a Compose file to configure your application's services. Then, using a single command, you create and start all the services from your configuration.”

