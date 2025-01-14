# Artifact Repository Manager with Nexus

<img src="images\12-nexus_ui.png">

## **Project Overview**
This project provides a high level overview of using Build Tools and Package Manager tools to build a Java and JavaScript application. It leverages code editor **IntelliJ** and build tools **Gradle**, **Maven**, **npm** and **nodeJS**. The project demonstrates how to build & package artifact as well as publishing an artifact.

---

## **Technologies**
- **Cloud Provider**: DigitalOcean
- **Linux Distribution**: Ubuntu
- **Java Build Tools**: Gradle, Maven
- **Artifact Repo Manager**: Nexus

---

## **Features**
- Install and configure Nexus from scratch on a cloud server
- Create new User on Nexus with relevant permissions
- Java Gradle Project: Build Jar & Upload to Nexus
- Java Maven Project: Build Jar & Upload to Nexus

---

## Steps to Install and Run Nexus on a cloud server

- Create Server (Resources with at least 4GB RAM / 2 CPUs)

- Install Java

```
apt update
apt install openjdk-17-jre-headless
java --version
```

- Configured Firewall

- Download Nexus

<img src="images\3-download-nexus.png">

<img src="images\3-download-nexus-pt2.png">

- Add Nexus User & Permissions

<img src="images\6-add_nexus_user.png">

<img src="images\7-add_nexus_permissions.png">

- Set Nexus Configuration

<img src="images\8-set_nexus_configuration.png">

- Run Nexus and verify

<img src="images\9-starting_nexus.png">


- Open Port to access the UI

<img src="images\10-open-port.png">

<img src="images\11-open-port-pt2.png">

## 

