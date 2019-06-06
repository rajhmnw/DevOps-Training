# Docker file apache image for DevOpsTrainingApp frontend
FROM ubuntu:18.04
MAINTAINER rajhmnw@gmail.com
# Adding user to kernel
#RUN useradd raj
# Enable user to execute the new command set
#USER raj
# Set CHROOT Work Directory
#WORKDIR /app
# To pass arguments with docker
#ARGV
#VOLUME
ENV TZ=Asia/Kolkata
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install nginx; apt-get -y install php; apt-get -y install php-gd; apt-get -y install php-mysql
# Copy the content of code folder to html folder
ADD code /var/www/html
# Copy the code folder to html folder
#COPY code/* /var/www/html
EXPOSE 80
ENV BACKENDDLB=test
# Absolute command to run apachectl without invoking shell, use square bracket and quote all the words separated by comma
CMD ["nginx", "-g", "daemon off;"]
# Entrypoint command cannot be replaced during the runtime
#ENTRYPOINT