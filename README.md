# fsnd-server-config

## Server
- Hostname: https://aws.luke.gr
- IP Address: 18.197.70.87
- SSH Port: 2200
- Web application: [aws.luke.gr](https://aws.luke.gr/)


## Software
- apache2
- libapache2-mod-wsgi
- postgresql
- virtualenv
- pip

### Python libraries
- flask
- sqlalchemy
- oauth2client
- httplib2
- requests


## Configuration
Listed below is a summary of steps taken to configure the server.

### General
- Created an Ubuntu Lightsail instance.
- Updated software package lists.
- Upgraded software packages.
- Configured appropriate DNS 'A' record for 'aws.luke.gr'.
- Configured SSH to operate on port 2200.

### Web application
- Installed apache2, libapache2-mod-wsgi, postgresql, virtualenv, and pip.
- Created and enabled an Apache site configuration file and corresponding application '.wsgi' file which imports my catalog project.
- Disabled the default Apache site.
- Updated the Google Credentials configuration and 'client_secrets.json' file.
- Set up the database with the project 'database_setup.py' file.

### User
- Created a 'grader' user.
- Assigned sudo permissions to 'grader'.
- Generated (locally) and installed a public-private key pair for 'grader' (with appropriate file and directory permissions).
- Forced key authentication over SSH.

### Firewall
- Denied all incoming traffic except for ports 80/tcp, 2200/tcp, 123/tcp.
- Allowed all outgoing traffic.
- Enabled the firewall.


## Third-party resources
- [How To Deploy a Flask Application on an Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
- [PIP Install: Unsupported locale setting](https://stackoverflow.com/questions/36394101/pip-install-locale-error-unsupported-locale-setting)
