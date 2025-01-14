# Infrastructure as a Service (IaaS) and DigitalOcean




## **Project Overview**
This project provides a high level overview of using Build Tools and Package Manager tools to build a Java and JavaScript application. It leverages code editor **IntelliJ** and build tools **Gradle**, **Maven**, **npm** and **nodeJS**. The project demonstrates how to build & package artifact as well as publishing an artifact.

---

## **Technologies**
- **Cloud Provider**: DigitalOcean
- **Linux Distribution**: Ubuntu
- **Java Build Tools**: Gradle, Maven
- **JavaScript Build Tools**: npm, nodeJS

---

## **Features**
- Create a virtual server on a cloud provider
- Deploy app on server and configure access
- Common concepts and best practices

---

## Setup Server on DigitalOcean

<img src="images\2-Create_Droplet.png">

- I logged into DigitalOcean and launched a Ubuntu droplet server with 4GBs and 2 CPUs.
    - Unfortunately, I couldn't take advantage of the free credits DigitalOcean as I have used the platform in the past.

- I also created a firewall for my droplet to allow only inbound connections from my PC's IP address. Without this step, anyone can attempt to brute force to log into the server.

- After logging into the new droplet server, I updated the apt package manager and installed Java

```
apt install update
apt install openjdk-8-jre-headless
```
<img src="images\4-Create_Droplet.png">

<img src="images\8-Create_Droplet.png">

---

## Deploying and running application artifact on Droplet

On my local PC, I built a Jar File and copied it over to my remote server and ran the application.

<img src="images\9-Create_Droplet.png">

<img src="images\11-Create_Droplet.png">

<img src="images\12-Create_Droplet.png">

## Configuring a Linux User on DigitalOcean

Utilizing best practices, I created a separate User and gave it only the permissions it needs to run the application.

<img src="images\1-Create_User.png">

<img src="images\2-Create_User.png">

<img src="images\4-Create_User.png">
