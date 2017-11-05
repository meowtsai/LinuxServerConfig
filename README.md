# Linux Server Configurations



## IP address
13.114.144.229 2200

## URL
- http://meowroll.com/  or
- http://13.114.144.229/


## Summary of software installed
 - `sudo apt-get install apache2`
 - `sudo apt-get install libapache2-mod-wsgi`
 - `sudo apt-get install python-pip`

## Summary of configurations made

- `/etc/ssh/sshd_config`
* `Port 2200`: change default ssh port to 2200.
* `PasswordAuthentication no`: passowrd login is not allwed.
* `PermitRootLogin no`: Log in as root remotely is not allowed.

- Firewall config
* Set up ufw and Amazon lightsail networking management panel to only allow connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).

- `/etc/apache2/sites-enabled/000-default.conf`
* config WSGI settings so it point to the right directory

- `sudo chmod 777 catalog-app`
* Change the permission of the web project folder so the database is accessible.


## third-party resources installed
- `sudo pip install virtualenv`
- `sudo pip install flask`
- `sudo pip install --upgrade google-auth`
- `sudo pip install SQLAlchemy`
- `sudo pip install --upgrade oauth2client`
- `sudo pip install requests`
