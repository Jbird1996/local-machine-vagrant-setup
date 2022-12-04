Setting up a web application using local VM's

1) Nginx Webserver
2) Tomcat Application server
3) RabbitMQ Broker/ queuing agent
4) Memcache DB caching
5) Elasticsearch Indexing/ search service
6) MySQL SQL database

Vagrant Up command to start up VM's

![image](https://user-images.githubusercontent.com/117186369/205487605-0b682970-db81-46d6-be55-7c0a9d5f9d0c.png)

Maria db installed on db01 server and running.

![image](https://user-images.githubusercontent.com/117186369/205489320-7606e91f-f252-4ef0-b39f-5b1ed3a88b5c.png)

Memcache running on MC01 server.

![image](https://user-images.githubusercontent.com/117186369/205491522-309c58ef-4b21-4d54-bef3-9c33910ddf47.png)

Install dependencies for RabbitMQ server.

sudo yum install wget -y

cd /tmp/

wget http://packages.erlang-solutions.com/erlang-solutions-2.0-1.noarch.rpm

sudo rpm -Uvh erlang-solutions-2.0-1.noarch.rpm

sudo yum -y install erlang socat

Install and start rabbitMQ

![image](https://user-images.githubusercontent.com/117186369/205492477-f623c8c5-26ea-4846-acb4-290a456af2bf.png)

Install and setup tomcat on app01 server

![image](https://user-images.githubusercontent.com/117186369/205497509-1037231c-18bf-4244-855a-e6bdbf0cc199.png)

