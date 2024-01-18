Network Security Project - README
Introduction
Attack is the Best Defense
In the dynamic landscape of cybersecurity, network security stands as a vital component. This project delves into tools and techniques commonly used in network security scenarios. The tools include Wireshark, Telnet, tcpdump, Docker, Hydra, and 0-0-sniffing.

Project Overview
What is This?
Security is a vast domain, and network security is critical due to the transmission of sensitive information over networks. Malicious entities can intercept network traffic, posing a threat to the confidentiality of data. This project explores the potential risks associated with unencrypted communication and the use of legacy systems, such as Telnet.

Sendgrid Integration
Sendgrid, a reputable email service, is introduced in the project. While it offers a secure system for sending emails, it also supports a legacy and unsecured method: Telnet. Users can create a free account on Sendgrid and utilize Telnet to send emails.

Task and Execution
Sniffing Unencrypted Traffic
The project focuses on sniffing unencrypted traffic to demonstrate the vulnerability of unsecured communication. A script, user_authenticating_into_server, is provided to simulate authentication steps. Participants are tasked with executing the script locally on their machines and using tcpdump to sniff the network and find a password.

Note: The script will not work on a Docker container or macOS. Participants are advised to use an Ubuntu vagrant machine or any other Linux machine.

You can download the script user_authenticating_into_server.

Solution
Obtaining the Password
Upon successful execution of the script, the ASCII code for the password is: bXlwYXNzd29yZDk4OTgh7.

Username: mylogin
Packet Sniffing
An example packet is provided to guide participants in identifying the password within the network traffic.

0000   d8 b6 b7 a1 1f 63 cc b0 da 2a bf b6 08 00 45 10   .....c...*....E.
0010   00 4a 40 f2 40 00 40 06 62 67 c0 a8 01 07 12 c5   .J@.@.@.bg......
0020   c2 d0 b5 12 02 4b 67 8b 60 d1 67 35 59 20 80 18   .....Kg.`.g5Y ..
0030   01 f5 a3 88 00 00 01 01 08 0a 21 35 2c 39 b2 84   ..........!5,9..
0040   5c 4c 62 58 6c 77 59 58 4e 7a 64 32 39 79 5a 44   \LbXlwYXNzd29yZD
0050   6b 34 4f 54 67 68 0d 0a                           k4OTgh..
Additional Challenge
1-dictionary_attack
Password-based authentication systems are susceptible to dictionary attacks. This challenge involves attempting a dictionary attack on an SSH account.

Install Docker on your Ubuntu Vagrant machine.
Pull and run the Docker image sylvainkalache/264-1 using the command docker run -p 2222:22 -d -ti sylvainkalache/264-1.
Obtain a password dictionary (you might need multiple).
Install and use Hydra to conduct a brute force attack on the SSH account 'sylvain' within the Docker container.
Since the Docker container is running locally, Hydra should access the SSH account via IP 127.0.0.1 and port 2222.
Hint: The password is 11 characters long.

