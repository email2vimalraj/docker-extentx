This repository contains **Dockerfile** of [ExtentX](https://github.com/anshooarora/extentx).

## Installation
1. Install [Docker](https://www.docker.com/)
2. Pull the **mongo** image from the docker hub: `docker pull mongo`
3. Pull the **extentx** image from the docker hub: `docker pull email2vimalraj/extentx`

## Usage
### Run Mongo server
```bash
docker run -p 27017:27017 -d --name extent-mongo mongo
```

### Run ExtentX
```bash
docker run --link extent-mongo:mongodb --name extent-app -p 1337:1337 -d email2vimalraj/extentx
```

Goto [http://localhost:1337](http://localhost:1337) in your browser to view the extentx dashboard.

**P.S**: Hit **Star** button if you found this useful.