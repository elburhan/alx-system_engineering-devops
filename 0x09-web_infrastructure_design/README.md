# Web Infrastructure Design

This repository contains whiteboard designs and explanations for various web infrastructure setups. Each task is aimed at demonstrating understanding and decision-making in designing web architectures.

## Table of Contents

- [Task 0: Simple Web Stack](#task-0-simple-web-stack)
- [Task 1: Distributed Web Infrastructure](#task-1-distributed-web-infrastructure)
- [Task 2: Secured and Monitored Web Infrastructure](#task-2-secured-and-monitored-web-infrastructure)
- [Task 3: Scale Up](#task-3-scale-up)

## Task 0: Simple Web Stack

### Design Overview

- **Server:** 1 server
- **Web Server:** Nginx
- **Application Server:** 1 application server
- **Application Files:** Your code base
- **Database:** MySQL
- **Domain Name:** www.foobar.com with a www record pointing to server IP 8.8.8.8

### Specifics

- **Server Role:** Hosts the entire web infrastructure.
- **Domain Name Role:** Resolves to the server's IP, making the website accessible.
- **Web Server Role:** Handles HTTP requests, serving static content.
- **Application Server Role:** Executes dynamic application logic.
- **Database Role:** Stores and retrieves data.

### Issues

- **Single Point of Failure (SPOF):** Entire system fails if any component fails.
- **Downtime:** Required for maintenance, as web server restarts affect service.
- **Scaling Limitation:** Unable to handle increased traffic.

### URLs


## Task 1: Distributed Web Infrastructure

### Design Overview

- **Servers:** 3 servers
- **Web Server:** Nginx
- **Application Server:** 1 application server per server
- **Load Balancer:** HAproxy
- **Application Files:** Your code base
- **Database:** MySQL

### Specifics

- **Additional Elements:** Added for redundancy and load distribution.
- **Load Balancer Algorithm:** Configured with (mention algorithm) for efficient distribution.
- **Active-Active or Active-Passive Setup:** Explain the chosen setup.
- **Primary-Replica (Master-Slave) Cluster:** Database replication for fault tolerance.
- **Difference Between Primary and Replica Nodes:** Explain in the context of the application.

### Issues

- **Single Points of Failure (SPOF):** Identify potential SPOFs.
- **Security Issues:** Lack of firewall and HTTPS.
- **No Monitoring:** Absence of monitoring for performance and security.

### URLs

- [GitHub Repository](link_to_repo)
- [Task 1 Screenshot](link_to_screenshot)

## Task 2: Secured and Monitored Web Infrastructure

### Design Overview

- **Servers:** 3 servers
- **Web Server:** Nginx
- **Application Server:** 1 application server per server
- **Load Balancer:** HAproxy
- **Firewalls:** 3 firewalls
- **SSL Certificate:** Serve www.foobar.com over HTTPS
- **Monitoring Clients:** 3 monitoring clients (Sumologic or other)

### Specifics

- **Additional Elements:** Added for security, encryption, and monitoring.
- **Firewall Role:** Protects against unauthorized access.
- **HTTPS Traffic:** Ensures encrypted communication.
- **Monitoring Role:** Collects data for analysis.
- **Monitoring Tool Data Collection:** Explain the data collection process.
- **Monitoring Web Server QPS:** Explain the approach.

### Issues

- **SSL Termination at Load Balancer:** Identify the issue.
- **Single MySQL Server for Writes:** Highlight the problem.
- **Uniform Server Components:** Explain potential problems.

### URLs

## Task 3: Scale Up

### Design Overview

- **Server:** 1 server
- **Load Balancer:** HAproxy configured as a cluster with another one
- **Split Components:** Web server, application server, database on their own server.

### Specifics

- **Additional Elements:** Added for scalability.
- **Load Balancer Cluster:** Configuration for load distribution and redundancy.

### URLs



