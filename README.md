# Hosting WordPress with Docker

WordPress is software designed for everyone, emphasizing accessibility, performance, security, and ease of use. We believe great software should work with minimum set up, so you can focus on sharing your story, product, or services freely. The basic WordPress software is simple and predictable so you can easily get started. It also offers powerful features for growth and success.

## Getting started

Bring up WordPress site is really easy by using this tool. All you have to do is clone the source and then run the script wordpress

### Clone the repo

```bash
git clone https://github.com/john-deng/docker-wordpress.git
```

### Change directory

```bash
cd docker-wordpress
```

### Type command ./install for the first time

```bash
./install
```

### or ./install -r if you want reset all settings

```bash
./install -r
```

wordpress will prompt below input requests, please input your site parameters or just type enter if your want to user the default settings

```bash

[INPUT] Domain [example.com]:
[INPUT] Email [your.name@example.com]:
[INPUT] MySQL root password [******]:
[INPUT] MySQL user password [******]:

Use example.com as your site domain? [yes/no] y

Done

```

### Or type command docker-compose up afterwards

```bash
docker-compose up -d
```

wordpress show up and running ...

```bash

Creating dockerwordpress_db_1 ... done
Creating dockerwordpress_wordpress_1 ... done

```

### Show docker-compose status

```bash
docker-compose ps
```

here is the status

```bash
           Name                          Command               State           Ports
--------------------------------------------------------------------------------------------
dockerwordpress_db_1          docker-entrypoint.sh mysqld      Up      3306/tcp
dockerwordpress_wordpress_1   docker-entrypoint.sh apach ...   Up      0.0.0.0:32823->80/tcp

```

### Shutdown wordpress

If you want to shutdown wordpress, just type docker-compose down

```bash
docker-compose down
```

```bash
Stopping dockerwordpress_wordpress_1 ... done
Stopping dockerwordpress_db_1        ... done
Removing dockerwordpress_wordpress_1 ... done
Removing dockerwordpress_db_1        ... done
Network web is external, skipping

```