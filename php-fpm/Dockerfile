FROM centos:7

MAINTAINER eddy147 <eddy147@gmail.com>

RUN yum -y --enablerepo=remi,remi-php56 install nginx php-fpm php-common
RUN yum -y --enablerepo=remi,remi-php56 install php-cli php-pear php-pdo php-mysqlnd php-pgsql php-gd php-mbstring php-mcrypt php-xml

COPY symfony.ini /etc/php5/fpm/conf.d/
COPY symfony.ini /etc/php5/cli/conf.d/
COPY symfony.pool.conf /etc/php5/fpm/pool.d/

CMD ["php5-fpm", "-F"]

EXPOSE 9000
