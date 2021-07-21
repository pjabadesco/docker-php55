docker run -it ubuntu
apt-get update
apt-get install apache2
apt-get install php libapache2-mod-php php-mcrypt php-mysql
apt-get install nodejs
apt-get install npm
npm install -g grunt-cli
service apache2 start
docker commit 3246225b5e98 ubuntu:angularjs
docker save ubuntu:angularjs > ubuntu_angularjs.tar
docker load < ubuntu_angularjs.tar
docker load < ubuntu_angularjs_ionic.tar




docker run -it php:5.5-cli bash
apt-get update
apt-get install git
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
mv composer.phar /usr/local/bin/composer
apt-get install apache2
Ctrl pq
docker commit 3246225b5e98 pjabadesco:php55
docker save pjabadesco:php55 > pjabadesco_php55.tar
docker load < pjabadesco_php55.tar

docker tag 4a7c8fdb2e90 pjabadesco/php55
docker push pjabadesco/php55
