opichon.docker-phpmyadmin
=========

Runs phpmyadmin as a docker container.

Requirements
------------

You need to have a mysql server running somewhere.

Role Variables
--------------

* phpmyadmin_absolute_uri: the uri
* phpmyadmin_mysql_hosts: the mysql hosts to which phpmyadmin provides access
* phpmyadmin_network: the name of the docker network which this container should join.
* phpmyadmin_state: started
* phpmyadmin_traefik_frontend_rule: the value of the traefirk.frontend.rule label. Ignore if you don't use a traefik proxy.
* phpmyadmin_traefik_priority: 1. the priority assigned to this host in traefik proxy. Ignore if you don;t use a traefik proxy.

Dependencies
------------

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - name: Deploy phpmyadmin
         	role: opichon.docker-phpmyadmin
         	phpmyadmin_absolute_uri: https://pma.mydomain.com
         	phpmyadmin_mysqlhosts: [mysql55, mysql56, mysql57]
         	phpmyadmin_network: default
         	phpmyadmin_traefik_frontend_rule: "Host:pma.mydomain.com"

License
-------

MIT
