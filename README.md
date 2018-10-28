# docker-mysql-apache2-

## mysql 

docker run --name mysql -e MYSQL_ROOT_PASSWORD=password -d -p 3306:3306 mysql

## phpmyadmin
	
docker run --name phpmyadmin -d --link mysql:db -p 7000:80 phpmyadmin/phpmyadmin

## apache2

sudo docker run -dit --name apache -p 8080:80 -v /home/user/website/:/usr/local/apache2/htdocs/ httpd
