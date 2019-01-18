Praktikum 4:

* apt-get update
* openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/apache-selfsigned.key -out /etc/ssl/certs/apache-selfsigned.crt
* peale seda tulevad promptid, kus Common name'i all kirjutasin oma ip (172.23.13.50)
* openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048
* nano /etc/apache2/conf-available/ssl-params.conf
* kopeerisin ülal oleva faili sisse pika teksti
* cp /etc/apache2/sites-available/default-ssl.conf /etc/apache2/sites-available/default-ssl.conf.bak (vastav käsk teeb backupi SSL Virtual host failile)
* nano /etc/apache2/sites-available/default-ssl.conf (täiendasin vastava faili enda serveri ip-ga ja muutsin ära osad failiteed)
* nano /etc/apache2/sites-available/000-default.conf (kirjutan juurde Redirect "/" "https://your_domain_or_IP/")
* käivitan moodulid:
 a2enmod ssl,
 a2enmod headers,
 a2ensite default-ssl,
 a2enconf ssl-params,
* apache2ctl configtest (kontrollib, kas kõik on töökorras)
* systemctl restart apache2
* lähen brauserisse ja kirjutan https://172.23.13.50
* praks tehtud
