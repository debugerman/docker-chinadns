chinadns + dnsmasq
==================

## About

- chinadns: Protect yourself against DNS poisoning in China.
- dnsmasq: A free software DNS forwarder and DHCP server for small networks.
- Forked from: https://github.com/vimagick/dockerfiles/tree/master/chinadns

## Docker Compose

    chinadns:
      image: vimagick/chinadns
      ports:
        - "53:53/udp"
        - "53:53/tcp"
      restart: always

## Run

    docker-compose up -d

## Test

    # UDP
    dig @127.0.0.1 www.google.com

    # TCP
    dig @127.0.0.1 www.youtube.com +tcp

