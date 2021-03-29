

Skip to content
Why GitHub? 
Team
Enterprise
Explore 
Marketplace
Pricing 
Search

Sign in
Sign up
culturadevops
/
jenkins
618
Code
Issues
Pull requests
2
Actions
Projects
Security
Insights
jenkins/jobs/dockerweb/Dockerfile
@jaivic
jaivic subiendo docker file
Latest commit 791a2e2 on 5 Feb 2020
 History
 1 contributor
19 lines (14 sloc)  516 Bytes
  
FROM php:7.1.17-apache
LABEL maintainer="Jaivic"

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y \
        zlib1g-dev \
        libicu-dev \
        libxml2-dev \
        libpq-dev\
	
        && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
        && docker-php-ext-install pdo pdo_mysql pdo_pgsql zip intl xmlrpc soap opcache \
        && docker-php-ext-configure pdo_mysql --with-pdo-mysql=mysqlnd \
        && apt-get install vim -y

COPY  . /var/www/html/
WORKDIR /var/www/html/

© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
