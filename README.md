<p align=center>
<p>
<img alt="ipfs" src="https://ipfs.io/ipfs/QmVk7srrwahXLNmcDYvyUEJptyoxpndnRa57YJ11L4jV26/ipfs.go.png" width="300" />
</p>
<p>
+
</p>
<p>
<img alt="caddy" src="https://cloud.githubusercontent.com/assets/1128849/25305033/12916fce-2731-11e7-86ec-580d4d31cb16.png" width="300" />
</p>
</p>
---

# IPFS-Gateway

The idea behind this project is to make tools/guides/etc to facilitate the process of making it easy to spin up your own ipfs gateway. It heavily relies on features of Caddy.


## Features

- Easy setup via docker or kubernetes
- Automatic HTTPS via Caddy
- Mount volume at `/data` for persistence.

## Docker Quickstart

Run this:

```docker run -d -e CADDYHOST=example.com -v `pwd`/data:/data -p 80:80 -p 443:443 --name ipfs-gateway cbluth/ipfs-gateway:latest```

In order for https to work, your host needs to be accessible on port 443 (hard requirement), and you need to set the `CADDYHOST` environment variable. If you do not want https, then do not set `CADDYHOST`.



## TODO

- Option to register ipfs-gateway on a public list
- Use `install.sh` to install locally.



