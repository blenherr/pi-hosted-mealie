# Install and setup instructions for Passbolt

## Introduction

[Passbolt](https://www.passbolt.com) is an open source password manager with [MariaDB](https://mariadb.com) backend. 

# Installation

## Install the App Template.

Goto App Templates and click on "Passbolt". Change Configuration to your needs:
- **PUID** (Enter your user's PUID here)
- **PGID** (Enter your user's PGID here)
- **TZ** (Enter your time zone here. See examples [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones))
- **MYSQL_ROOT_PASSWORD** (Enter your MySql root password here)
- **MYSQL_DATABASE** (Enter your Passbolt database name here)
- **MYSQL_USER** (Enter your Passbolt database user here)
- **MYSQL_PASSWORD** (Enter your Passbolt database password here)
- **APP_FULL_BASE_URL** (Enter your full Passbolt https base URL here. Including port if different from 443)
- **PASSBOLT_PORT** (Enter your Passbolt https port here)

## Setup Passbolt admin user

Go into Passbolt container console.
Type in the code below and change it to your needs:
```
su -s /bin/bash -c "./bin/cake passbolt register_user -u youremail@mail.net -f yourfirstname -l yourlastname -r admin" www-data
```
After that you get something like this:
```
     ____                  __          ____  
    / __ \____  _____ ____/ /_  ____  / / /_ 
   / /_/ / __ `/ ___/ ___/ __ \/ __ \/ / __/ 
  / ____/ /_/ (__  |__  ) /_/ / /_/ / / /    
 /_/    \__,_/____/____/_.___/\____/_/\__/   

 Open source password manager for teams
-------------------------------------------------------------------------------
User saved successfully.
To start registration follow the link provided in your mailbox or here: 
https://passbolt.local/setup/start/9fb7180d-b44b-41bf-bf77-8c5ab23e8cbc/966ce549-18ec-4b12-9171-9a1bb2f1a393
```
Copy and paste the url above in browser. Proceed with `Welcome to Passbolt, please select a passphrase!`.

You may have to install Passbolt browser add-on.

## After admin user activation
Configure Email server by clicking on administration
