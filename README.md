## Running it
ON the host system:
1. `$ docker-compose up -d`

## Arming the alert
In the Kapacitor container:
1. `$ kapacitor define alert -type stream -tick alert.tick -dbrp telegraf.autogen`
2. `$ kapacitor enable alert`

## Generating traffic
On the host system running docker-compose:
1. `$ cat sample | nc localhost 8094`
