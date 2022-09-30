# grabs latestest version of ubuntu
FROM ubuntu:latest

# updates all the packages
RUN apt-get -y update

# this will install apache 2 and curl will make sure that it is running
RUN apt-get install -y apache2 curl

# this the directory where the container will work from
WORKDIR /var/www/html

# copy the index.html from the host to this path inside the container and replace the existing one
COPY index.html /var/www/html/index.html

EXPOSE 80

# command that will start the apache service
ENTRYPOINT [ "usr/sbin/apache2ctl" ]

# entry point will use the CMD flags as the command
CMD ["-D", "FOREGROUND"]