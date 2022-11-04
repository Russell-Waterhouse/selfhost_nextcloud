# Self Hosted Nextcloud Configuration
A docker-compose file and readme for people to use to setup their own nextcloud instance

## Configuration: 
In the docker-compose.yml file, replace 
```
{ROOT PASSWORD HERE}
{PASSWORD HERE} 
{HOSTNAME HERE}
```
with a strong and complex root password, user password
and whatever hostname you wish to use.   

I just appended a hostname entry to my /etc/hosts file on the linux machines that I plan 
to access my nextcloud instance from. For individual users, nothing more complicated is necessary. 
For enterprise users who wish to buy a domain name or 

## Installation
run 
```bash
docker-compose up -d
```

Wait a minute for everything to come online. 

In a browser, go to https://{HOST IP}, and follow the setup instructions. 
Make sure that you select mariadb/mysql and enter the following information
``` 
username: nextcloud
database: nextcloud
password: {PASSWORD HERE}
host: db:3306
```


## Optional Steps
To access your self-hosted nextcloud instance from anywhere in the world, not just on your 
local network, you can setup [tailscale](https://tailscale.com/) on whatever devices
you plan to access your nextcloud instance from. 
