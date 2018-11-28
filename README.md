# My_Docker_Notes

## mysql 

docker run --name mysql -e MYSQL_ROOT_PASSWORD=password -d -p 3306:3306 mysql

## phpmyadmin
	
docker run --name phpmyadmin -d --link mysql:db -p 7000:80 phpmyadmin/phpmyadmin

## apache2

docker run -dit --name apache -p 8080:80 -v /home/user/website/:/usr/local/apache2/htdocs/ httpd

## mongoDB

docker run --name <YOUR-NAME> -p 27017:27017 -v /data/db:/data/db -d mongo
- v分號前面的代表主機的位置 
