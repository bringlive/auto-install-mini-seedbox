# Auto Install Script Rtorrent + Rutorrent + Libtorrent

All in One installer script by me, a modified version of [Bercik1337](https://github.com/Bercik1337/rt-auto-install) and [MarkusLange](https://github.com/MarkusLange/rt-auto-install) script what is a modified version of Kerwood's script.

### Modern script for automatic rtorrent, rutorrent and libtorrent installation under Linux.
	Makes your system seedbox ready in minutes!

![Logo](https://i.imgur.com/KtvJriL.jpg)

## News

**Current version** v2.5 released 2026/01/20

	* always use of the latest ruTorrent
	* no need to care about the distro version
	* remove unnecessary stuff
	* add support for arm* systems (scgi)
	* correcting external ipv4
	* deactivate not supportet plugins
	* redirect http to https
	* correct terminal colors
	* add autodl-irssi plugin (Rt-Install-minimal-new.bash)
	* update .rtorrent.rc to the new commands
	* fix changelog and todo view
	* put functions together for more order
	* make pre-installation packages fully silent
	* and a little bit there and there
	* now choose between apache2, nginx and lighttpd as webserver (Rt-Install-minimal-apache2_nginx_lighttpd_prc-socket_choose_branche)
	* create htaccess passwords now with openssl
	* remove ToDo-List from the Menu
	* move from SCGIMount to rpc.socket
	* hardening the webserver basend on https://raymii.org/s/tutorials/Strong_SSL_Security_On_*.html
	* reintegrade To-Do List
	* putting rtorrent and rutorrent user determination inside the menu and prevent installation to start without
	* add function to update ruTorrent
	* reactivate plugins screenshots, spectrogram
	* some corrections
	* adopt the actual ruTorrent branches (v4 & v5) since autodl is brocken in v5

## Features ##

* This script performs automatic installation of rTorrent (BitTorrent client), ruTorrent (web based GUI) and libTorrent (BitTorrent protocol).
* It detects your OS and uses most recent version of rT available in repository of your Linux distribution.
* Gives menu-driven guidance when creating username.
* This script is minimal inversiv to files and operating system
* Free choose between apache2, nginx or lighttpd as webserver

## Supported operating systems ##

* **Debian**
* **Raspbian**
* **Ubuntu**
* **Mint**
* **LMDE**

## What the scripts does ##
In the installation process you have to choose a system user to run rtorrent. The script add a service that
makes rtorrent start, at a possible reboot, in the given username's tmux session. Use "systemctl rtorrent start"
and "systemctl rtorrent stop" to start and stop rtorrent respectively.

### Run the script with sudo or as root:
  1. git clone https://github.com/bringlive/auto-install-rTorrent-ruTorrent-libTorrent.git
  2. cd auto-install-rTorrent-ruTorrent-libTorrent
  3. chmod +x Rt-Install-minimal-apache2_nginx_lighttpd_prc-socket_choose_branche.bash
  4. sudo ./Rt-Install-minimal-apache2_nginx_lighttpd_prc-socket_choose_branche.bash

### Or:
  1. wget https://raw.githubusercontent.com/MarkusLange/rt-auto-install/master/Rt-Install-minimal-apache2_ngnix_lighttpd_prc-socket_choose_branche.bash
  2. curl -L https://raw.githubusercontent.com/MarkusLange/rt-auto-install/master/Rt-Install-minimal-apache2_ngnix_lighttpd_prc-socket_choose_branche.bash -o rt-install.bash
  
### If You Too Lazy
  1. git clone https://github.com/bringlive/auto-install-rTorrent-ruTorrent-libTorrent.git && cd auto-install-rTorrent-ruTorrent-libTorrent && chmod +x Rt-Install-minimal-apache2_nginx_lighttpd_prc-socket_choose_branche.bash && sudo ./Rt-Install-minimal-apache2_nginx_lighttpd_prc-socket_choose_branche.bash
  2. wget https://raw.githubusercontent.com/MarkusLange/rt-auto-install/master/Rt-Install-minimal-apache2_ngnix_lighttpd_prc-socket_choose_branche.bash && chmod +x Rt-Install-minimal-apache2_nginx_lighttpd_prc-socket_choose_branche.bash && sudo ./Rt-Install-minimal-apache2_nginx_lighttpd_prc-socket_choose_branche.bash
  3. curl -L https://raw.githubusercontent.com/MarkusLange/rt-auto-install/master/Rt-Install-minimal-apache2_ngnix_lighttpd_prc-socket_choose_branche.bash -o rt-install.bash && chmod +x rt-install.bash && sudo ./rt-install.bash


## NOTE
1. Make sure run with sudo and "adduser [your desire username]" before run the script
2. If you find "dump" plugin not work, you have to install [dumptorrent](https://github.com/bringlive/auto-install-rTorrent-ruTorrent-libTorrent/releases/download/etc/dumptorrent_1.7.0-ubuntu-latest_amd64.deb) then install it with "sudo dpkg -i dumptorrent_1.7.0-ubuntu-latest_amd64.deb"
