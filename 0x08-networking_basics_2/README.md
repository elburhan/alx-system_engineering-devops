Project Title: Networking Basics 2
Overview
This project consists of a series of Bash scripts aimed at configuring an Ubuntu server, displaying active IPv4 IPs, and creating a script for port listening on localhost.

Repository Information
GitHub Repository: alx-system_engineering-devops
Directory: 0x08-networking_basics_2
Task 0: Change Your Home IP
Description
Write a Bash script that configures an Ubuntu server to change the IP addresses for localhost and facebook.com.

Requirements
localhost should resolve to 127.0.0.2
facebook.com should resolve to 8.8.8.8
Checker runs on Docker (consider this in the script)
Usage Example
bash
Copy code
sylvain@ubuntu$ ping localhost
# Output: PING localhost (127.0.0.1) ...

sylvain@ubuntu$ ping facebook.com
# Output: PING facebook.com (157.240.11.35) ...

sylvain@ubuntu$ sudo ./0-change_your_home_IP
sylvain@ubuntu$

sylvain@ubuntu$ ping localhost
# Output: PING localhost (127.0.0.2) ...

sylvain@ubuntu$ ping facebook.com
# Output: PING facebook.com (8.8.8.8) ...
Important Note
If running the script on a machine intended for continued use, revert localhost to 127.0.0.1 afterward.

Task 1: Show Attached IPs
Description
Write a Bash script that displays all active IPv4 IPs on the machine where it's executed.

Usage Example
bash
Copy code
sylvain@ubuntu$ ./1-show_attached_IPs | cat -e
# Output:
10.0.2.15$
127.0.0.1$
sylvain@ubuntu$
Task 2: Port Listening on Localhost
Description
Write a Bash script that listens on port 98 on localhost and demonstrates communication using telnet.

Advanced
This script allows for testing connections within localhost and across networks.

Usage Example
Terminal 0:

bash
Copy code
sylvain@ubuntu$ sudo ./100-port_listening_on_localhost
Terminal 1:

bash
Copy code
sylvain@ubuntu$ telnet localhost 98
# Output: Connected to localhost. Escape character is '^]'.
Hello world
test
Terminal 0 (Receiving):

bash
Copy code
sylvain@ubuntu$ sudo ./100-port_listening_on_localhost
# Output:
Hello world
test
Note
This script is versatile and can be used for debugging socket connection issues, testing software connections, and debugging firewall rules.

Conclusion
These scripts enhance Ubuntu server configuration, provide information on active IPv4 IPs, and offer a versatile tool for testing and debugging network connections. Feel free to contribute or suggest improvements!
