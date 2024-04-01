#### (tested on ubuntu 22.04)

### This repo is build based on blog article:
https://www.elastic.co/blog/getting-started-with-the-elastic-stack-and-docker-compose

### Copy .env_example to .env
```
cp .env_example .env
```

### change permissions (if needed)
```
sudo chmod go-w ./filebeat.yml
sudo chown root:root filebeat.yml

sudo chmod go-w ./metricbeat.yml
sudo chown root:root metricbeat.yml
```

### Steps:
```
docker compose build --pull
```
```
docker compose up
```
Some issues? (only example)
```
docker compose up | grep -E 'WARN|ERROR'
```

In browser:
http://0.0.0.0:5601/
