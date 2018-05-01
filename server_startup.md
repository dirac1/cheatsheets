Server Startup suggestions (SSS) 
===========================================
PAM & SSH
---------
* Configure Locales and keyboard binding
* Change root password
* Create new user and admin group 
* Install sudo and add admin group and user to sudo using visudo
* Install zsh and oh-my-zsh
* Disable root login via ssh, limit authentication methods to just user and admin group, and limit the authentication times 
* Use public keys for the admin user
* Install fail2ban and configure ssh module, white list your local IP ranges
* Optional: Renew user password every 1 month
* Optional: Install tmux and get tmux plugin manager tpm for multiplexing windows
* Optional: Renew user password every 1 month
* Optional: Install msmtp to notify via email fail2ban bans 

Processes
---------
* Install htop to monitor processes

Network & Services
------------------
* Enable forwarding via kernel, configure Iptables to protect your services and block the rest
* Harden your kernel options principally Ipv4-6 options
* O install wget,curl,aria2,git
* O install trizen (archlinux only)
* PSAD 


cool commands expac '%m\t%n' | sort -h (sort packages sizes)
sudo pacman -R $(pacman -Qdtq) delete unneeded packages
