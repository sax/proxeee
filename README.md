proxeee
=======

Proxy requests to S3 with a cache, using Nginx.

## Setup

Install dependencies:

```bash
brew bundle
```

Nginx will start on a non-privileged port. To configure port forwarding, use the
following:

El Capitan:

```bash
sudo ln -s "${PATH_TO_PROXEEE}/port_forwarding/el_capitan/com.proxeee" /etc/pf.anchors/com.proxeee
sudo ln -s "${PATH_TO_PROXEEE}/port_forwarding/el_capitan/pf-proxeee.com" /etc/pf-proxeee.conf

# Enable port forwarding
sudo pfctl -ef /etc/pf-proxeee.conf

# Disable port forwarding
sudo pfctl -df /etc/pf-proxeee.conf
```


## Usage

```bash
nginx -c ${PWD}/nginx.conf
```

