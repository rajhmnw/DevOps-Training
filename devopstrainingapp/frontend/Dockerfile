# Docker file apache image for DevOpsTrainingApp frontend
FROM centos:7
MAINTAINER rajhmnw@gmail.com
# Adding user to kernal
#RUN useradd raj
# Enable user to execute the new command set
#USER raj
# Set CHROOT Work Directory
#WORKDIR /app
# To pass arguments with docker
#ARGV
#VOLUME
RUN yum -y update
RUN yum -y install httpd
# Copy the content of code folder to html folder
ADD code /var/www/html
# Copy the code folder to html folder
#COPY code/* /var/www/html
EXPOSE 80
ENV BACKENDDLB=test
# Absolute command to run apachectl without invoking shell, use square bracket and quote all the words separated by comma
CMD ["apachectl", "-D", "FOREGROUND"]
# Entrypoint command cannot be replaced during the runtime
#ENTRYPOINT