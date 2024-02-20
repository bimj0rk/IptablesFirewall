# IptablesFirewall
A firewall made using Kali Linux and Iptables with a test attack

The app is specifially designed for Linux users with Iptables and UFW installed and running. To launch it, run the script file in the terminal of the Operating System. 

The user interface was created using whiptail and it is easy and intuitive.

The main features of the firewall are as follows:
  -blocks incoming packets that enter from an external machine that claims to be inside the network. The attacker usually uses a specific port (usually eth0), and this can be used to our advantage.
  -drops every package that has a SYNCHRONIZED (SYN) flag
  -limits the number a fragments a packet can be divided into

I also created an attack (not recommended outside of testing purposes) used to test the funcionalities. 
