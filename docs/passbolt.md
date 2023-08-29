# Install and setup instructions for Passbolt

## Introduction

 is an open source password manager with ![MariaDB](https://mariadb.com) backend. 

# Installation

## Install the App Template.

Goto App Templates and click on "Passbolt". Change Configuration to your needs:
- MariaDB PUID (PUID of your user)
- MariaDB PGID (PGID of your user)
- MariaDB Timezone (![Timezone list](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones))
- MariaDB root password (Choose a password)
- Passbolt database name (Choose a name)
- Passbolt database user (Choose a user)
- Passbolt database password (Choose a password)
- Passbolt full HTTPS base URL (Full https base URL including port if differs to 443)
- Passbolt HTTPS port (Choose a port)

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

You may have to install Passbolt Add-on.
