# socks5-server

A socks5 server(tcp/udp) written in golang.

[![Travis](https://travis-ci.com/net-byte/socks5-server.svg?branch=main)](https://github.com/net-byte/socks5-server)
[![Go Report Card](https://goreportcard.com/badge/github.com/net-byte/socks5-server)](https://goreportcard.com/report/github.com/net-byte/socks5-server)
![image](https://img.shields.io/badge/License-MIT-orange)
![image](https://img.shields.io/badge/License-Anti--996-red)

# Usage
```
Usage of /main:
  -l string
        local address (default "127.0.0.1:1080")
  -p string
        password
  -u string
        username
```

# Docker

## Run server
```
docker run  -d --restart=always --net=host \
-p 127.0.0.1:1080:1080 -p 127.0.0.1:1080:1080/udp --name socks5-server netbyte/socks5-server -l 127.0.0.1:1080
```

## Run server with auth
```
docker run  -d --restart=always --net=host \
-p 127.0.0.1:1080:1080 -p 127.0.0.1:1080:1080/udp --name socks5-server netbyte/socks5-server -l 127.0.0.1:1080 -u root -p 123456
```

# License
[The MIT License (MIT)](https://raw.githubusercontent.com/net-byte/opensocks/main/LICENSE)


