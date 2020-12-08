# grafana

Documentation and source code for the departmental grafana applaince served at https://grafana.chem.wisc.edu.

To prepare (starting with Ubuntu 20.04)
```
$ apt install docker.io
$ apt install docker-compose
```

This machine needs the following ports to be open to the campus network:
- 80 (http) (used via reverse proxy)

To run:
```
$ docker-compose up -d --build
```

Volumes:

This compose file will create a docker volume `grafana_grafana`.
On the host machine it appears at `/var/lib/docker/volumes/grafana_grafana/`.

Users:

This machine integrates with departmental LDAP for user authentication.
All chemistry users are editors of one pool of dashboards.
By design, there is no admin account.
