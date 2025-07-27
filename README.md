# PARKEDNS

## Install

### Alternatif A

```
mkdir -p parkedns
docker run -d --name parkedns --restart unless-stopped -p 8080:80 -v ./parkedns:/parkedns ghcr.io/erolj/parkedns:latest
```

### Alternatif B

```
git clone https://github.com/erolj/parkedns.git
cd parkedns
docker compose up -d
```

## Update

### Alternatif A

```
docker pull ghcr.io/erolj/parkedns:latest
docker kill parkedns
docker rm parkedns
docker run -d --name parkedns --restart unless-stopped -p 8080:80 -v ./parkedns:/parkedns ghcr.io/erolj/parkedns:latest
```

### Alternatif B

```
git pull
docker kill parkedns
docker rm parkedns
docker compose up -d
```
