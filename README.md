# Synopsis

**zerauth** is a ZeroShell auto-login daemon. It can handle unstable
connections and reconnects itself when the renewal requests timeout.

# Requirements

* python3
* pip-3

# Install

    $ git clone https://github.com/mrteera/zerauth
    $ cd zerauth
    $ pip3 install -r requirements.txt

# Config

    $ vim zerauth.conf

    login:
        username:               # Your username
        password:               # Your password
        domain:                 # The domain 

    server:
        host: 192.168.0.1       # The hostname / IP of the captive portal
        port: 12080             # The port associated with the right protocol
        protocol: http          # http or https (must match with 'port')
        renew_delay: 40         # Seconds between each renew request
        
# Usage

    $ python3 zerauth.py
