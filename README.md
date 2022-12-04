# Setting up a web application on local VM's using vagrant.

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

Install and setup nginx 

Create a configuration file that will be used to redirect requests from nginx to tomcat server on port 8080.

![image](https://user-images.githubusercontent.com/117186369/205498898-486dfa8a-38ed-47d4-bdab-59aa6366aabf.png)

remove default website of nginx

rm -rf /etc/nginx/sites-enabled/default

create link of configuration file. 

ln -s /etc/nginx/sites-available/vproapp /etc/nginx/sites-enabled/vproapp

![image](https://user-images.githubusercontent.com/117186369/205499418-5803adb9-2cd7-4d2d-aa15-87d0191463fc.png)

Get IP address of webserver.

![image](https://user-images.githubusercontent.com/117186369/205499616-34c98a24-d696-4081-bfb3-9de9a699d31b.png)

End result of project.

![image](https://user-images.githubusercontent.com/117186369/205499587-4df2aa98-f50b-4562-857e-ac54decf5085.png)




 
 

