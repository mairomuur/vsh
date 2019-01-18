Praktikum 6:

 apache masina tegevused: 
* installeerisin apache2 - apt-get install apache2
* installeerisin php - apt install php5
* apt-get install mysql-server php5-mysql
* wordpressi commandid:
* cd /var/www/html/
* wget http://wordpress.org/latest.zip
* aptitude install unzip
* unzip -q latest.zip
* chown -R www-data:www-data /var/www/html/wordpress
* chmod -R 755 /var/www/html/wordpress
* mkdir -p /var/www/html/wordpress/wp-content/uploads
* chown -R www-data:www-data /var/www/html/wordpress/wp-content/uploads

db masina tegevused:
* mysql -u root -p
* create database tere;
* create user kasutaja@10.0.2.6;
* grant all privileges on tere.* to kasutaja@10.0.2.6;
* flush priviletges
* exit
Installeerisin ubuntu kliendi, et testida, kas wordpress töötab
* kirjutasin ubuntu kliendi brauserisse 10.0.2.4/wordpress 
