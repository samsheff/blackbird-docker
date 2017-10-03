#blackbird meets Docker
This is a simple Docker container for blackbird, a Bitcoin Arbitrage Bot. The one currently in master in the official repo was out of date and not building.

The Dockerfile pulls the current source, installs the dependencies and installs it.

## How to ...?

If you prefer to build the container yourself

```bash
$ git clone https://github.com/samsheff/blackbird-docker
$ cd blackbird-docker
$ docker build -t blackbird .
```

If you *trust me* and prefer to download it directly from Docker Hub

```bash
$ docker pull samsheff/blackbird
```

either way, then you can run it (after editing the config file and adding api keys) by executing

```bash
$ docker run -it samsheff/blackbird
```
