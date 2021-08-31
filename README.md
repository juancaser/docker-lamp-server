# Yet another docker lamp-server
This is just one of docker lamp-server you can find in the internet.

## How to use

Using this docker compose is as easy as walk in the park, you just need to run the command in your favorite console/terminal. But make sure you you properly install docker first otherwise it wont work.

```
$ docker-compose up -d
```

## Entering container shell

You may need to enter the shell like enabling some apache module or installing some php extension. Docker Destkop actually provides an easy way to the shell, but you can also enter via terminal.

```
$ docker exec -it webserver /bin/bash
```

```webserver``` is the default name of your container, if you renamed it use that one instead.

## Enabling/Disabling Apache module

See Entering container shell for instruction how to access it.

#### To enable

```a2enmod <name of module> ```

#### To disable

```a2dismod <name of module> ```

To properly run the webserver and use the virtual hostname and url rewrite you need to enable this apache module


 ```a2enmod vhost_alias```

 ```a2enmod rewrite```

The after any changes you can restart apache or restart the whole container via Docker Desktop

 ```server apache2 restart```

