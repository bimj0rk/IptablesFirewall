# Iptables Firewall (Computer Networks project, Year III)
### by Adrian Campean ([@bimj0rk](https://github.com/bimj0rk)), Dan Deaconu ([@DoubleDew](https://github.com/DoubleDew)) and Darius Nazemian ([@dariusnp](https://github.com/dariusnp))
A firewall made using Kali Linux and Iptables with a test attack
The app is specifially designed for Linux users with Iptables and UFW installed and running. To launch it, run the script file in the terminal of the Operating System. 

### Features
The main features of the firewall are as follows:
  * blocks incoming packets that enter from an external machine that claims to be inside the network. The attacker usually uses a specific port (usually eth0), and this can be used to our advantage.
  * drops every packet that has a SYNCHRONIZED (SYN) flag
  * limits the number a fragments a packet can be divided into

### User interface
![Picture 0](https://github.com/bimj0rk/IptablesFirewall/assets/37622282/70ce0750-a89e-4bd8-9267-154fdfb60e30)

There are four main menus for the firewall:
 * Start firewall: start and stops the firewall; if the chosen option is already selected, the user gets warned about it (this is done by saving the state of the firewall in a log file);

![Picture 1](https://github.com/bimj0rk/IptablesFirewall/assets/37622282/b2889cfc-4bd9-48c1-94e5-d85f24f3016b)
 * Statistics: using netstat, statistics about network usage is saved in another log file and then outputed to the user;

![Picture 2](https://github.com/bimj0rk/IptablesFirewall/assets/37622282/6fc3dc6d-985d-41f0-9bb1-ca5fed59725b)
 * Rules: shows the iptables rules the user has set

![Picture 3](https://github.com/bimj0rk/IptablesFirewall/assets/37622282/52ab46d0-c4b0-4466-b42c-18568906ebb5)
 * Settings: this is where the user can add or enable certain features (insert custom rule, delete rule, add a rule to a certain position in the chain, drop strange packets, track and drop SYN packets and limit the number of fragments a packet can have).

![Picture 4](https://github.com/bimj0rk/IptablesFirewall/assets/37622282/438cc01f-3079-4bec-b6a6-016c6ee18803)

### Test attack
For testing purposes, we also created an attack in Python, using [Scapy](https://scapy.net/), that sends packets from a source with the IP address of 150.x.x.x, with SYN flags and fragmentted to 2048 fragments.
