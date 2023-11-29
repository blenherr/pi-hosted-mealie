# Install and setup instructions for scrutiny

- [Introduction](#introduction)
- [Installation](#installation)
- [Setup first admin user](#setup-first-admin-user)
- [Setup Android Mobile App](#setup-android-mobile-app)
- [Acknowledgment / Troubleshoot](#acknowledgment--troubleshoot)


## Introduction

[Scrutiny](https://www.passbolt.com) is an WebUI for smartd S.M.A.R.T monitoring with [InfluxDB](https://www.influxdata.com) backend. 

## Installation

### Pre-Installation Steps

Create directorys:
```
sudo mkdir /portainer/Files/AppData/Config/passbolt && \
sudo mkdir /portainer/Files/AppData/Config/passbolt/certs
```

### Install the App Template.

Goto App Templates and click on "Passbolt". Change Configuration to your needs:
- **PUID** (Enter your user's PUID here)
- **PGID** (Enter your user's PGID here)
- **TZ** (Enter your time zone here. See examples [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones))
- **MYSQL_ROOT_PASSWORD** (Enter your MySql root password here)
- **MYSQL_DATABASE** (Enter your Passbolt database name here)
- **MYSQL_USER** (Enter your Passbolt database user here)
- **MYSQL_PASSWORD** (Enter your Passbolt database password here)
- **PASSBOLT_PORT** (Enter your Passbolt https port here)
- **PASSBOLT_URL** (Enter your full Passbolt https base URL here. Including port if different from 443)
- **EMAIL_FROM_NAME** (Enter your from email name)
- **EMAIL_FROM_ADDRESS** (Enter your from email address)
- **EMAIL_SMTP_SERVER** (Enter your email smtp server here)
- **EMAIL_SMTP_PORT** (Enter your email smtp port here)
- **EMAIL_USERNAME** (Enter your email username here)
- **EMAIL_PASSWORD** (Enter your email password here)
- **EMAIL_TLS** (Enter set TLS here)

## Setup first admin user

Go into Passbolt container console. Type in the code below and change it to your needs:
```
su -s /bin/bash -c "./bin/cake \
    passbolt register_user \
    -u youremail@mail.net \
    -f yourfirstname \
    -l yourlastname \
    -r admin" www-data
```

## Acknowledgment / Troubleshoot
- GitHub: [https://github.com/AnalogJ/scrutiny](https://github.com/AnalogJ/scrutiny)
