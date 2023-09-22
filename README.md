# Kingsley Documentation of Project 8
### LOAD BALANCER SOLUTION WITH APACHE

#Introduction

After completing Project-7 one might wonder how a user will be accessing each of the webservers using 3 different IP address or 3 different DNS names. You might also wonder what is the point of having 3 different servers doing exactly the same thing.

When we access a website in the Internet we use an URL and we do not really know how many servers are out there serving our requests, this complexity is hidden from a regular user, but in case of websites that are being visited by millions of users per day (like Google or Reddit) it is impossible to serve all the users from a single Web Server (it is also applicable to databases, but for now we will not focus on distributed DBs).

In our set up in Project-7 we had 3 Web Servers and each of them had its own public IP address and public DNS name. A client has to access them by using different URLs, which is not a nice user experience to remember addresses/names of even 3 server, let alone millions of Google servers.

In order to hide all this complexity and to have a single point of access with a single public IP address/name, a Load Balancer can be used. A Load Balancer (LB) distributes clients’ requests among underlying Web Servers and makes sure that the load is distributed in an optimal way.

### Task

*Deploy and configure an Apache Load Balancer for Tooling Website solution on a separate Ubuntu EC2 intance. Make sure that users can be served by Web servers through the Load Balancer*

### Steps - Configure Apache As A Load Balancer

1. Create an Ubuntu Server 20.04 EC2 instance and name it Project-8-apache-lb, so your EC2

2. Open TCP port 80 on Project8-apache-lb by creating an Inbound Rule in Security Group.

3. Install Apache Load Balancer on Project8-apache-lb server and configure it to point traffic coming to LB to both Web Servers

4. Verify that our configuration works – try to access your LB’s public IP address or Public DNS name from your browser

### Optional Step – Configure Local DNS Names Resolution
