# Elevate-Labs-Tasks-4

Task 4

# Setup and Use a Firewall on Windows/Linux

## Objective
Configure and test basic firewall rules to allow or block traffic.

### Tools Used

- **Kali Linux** for penetration testing and security auditing.
- **Windows Firewall / UFW (Uncomplicated Firewall) on Linux.** Windows Firewall / UFW on Linux are used to control network traffic by allowing or blocking connections for system security
## Steps

Below are the key steps taken in this process:

### 1. Updating Packages and Installing UFW on Ubuntu

- sudo apt update
- sudo apt install ufw -y

![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-4/blob/main/Screenshot%202025-09-28%20192003.png)

### 2. List current firewall rules.

sudo ufw status numbered


![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-4/blob/main/Screenshot%202025-09-28%20192320.png)




### 3. Add a rule to block inbound traffic on a specific port (e.g., 23 for Telnet).

sudo ufw deny proto tcp from any to any port 23 comment 'Block-Telnet'


![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-4/blob/main/Screenshot%202025-09-28%20192445.png)
 

### 4. Add rule to alow SSH (port 22) if on Linux

- sudo ufw allow 22/tcp
- sudo ufw allow ssh
- sudo ufw enable
- sudo ufw status numbered

![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-4/blob/main/Screenshot%202025-09-28%20212146.png)

### 5. Remove the test block rule to restore original state

sudo ufw delete 1
sudo ufw delete 2

![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-4/blob/main/Screenshot%202025-09-28%20214200.png)

### 5. Conclusion

successfully configured and tested firewall rules to allow or block traffic, gaining hands-on experience in managing network traffic and understanding how firewalls filter connections to enhance system security.
