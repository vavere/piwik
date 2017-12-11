# Piwik

Piwik is the leading open-source analytics platform that gives you more than just powerful analytics:

 - Free open-source software
 - 100% data ownership
 - User privacy protection
 - User-centric insights
 - Customisable and extensible

# How to use this image

The easiest is to use our `docker-compose.yml`.

Make sure you have [docker-compose](http://docs.docker.com/compose/install/) installed. And then:

```bash
git clone https://github.com/indiehosters/piwik.git
cd piwik
MYSQL_ROOT_PASSWORD=mystrongpassword docker-compose up
```

You can now access your instance on the port 80 of the IP of your machine (not recommended for production).

## Access it from Internet

We recommend the usage of TLS, so the easiest is to use a TLS capable reverse proxy.
Here are 2 examples:

 - [haproxy](https://github.com/indiehosters/haproxy)
 - [nginx](https://github.com/indiehosters/nginx)

You can also modify manually the nginx configuration file and map the TLS port of the host to the container.

## Installation

Once started, you'll arrive at the configuration wizard.
At the `Database Setup` step, please enter the following:

  -  Database Server: `db`
  -  Login: `root`
  -  Password: MYSQL_ROOT_PASSWORD
  -  Database Name: piwik (or you can choose)
 
And leave the rest as default.

Then you can continue the installation with the super user.

