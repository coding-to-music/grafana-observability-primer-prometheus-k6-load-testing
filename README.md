# grafana-observability-primer-prometheus-k6-load-testing

# 🚀 Grafana Observability Primer 🚀

https://github.com/coding-to-music/grafana-observability-primer-prometheus-k6-load-testing

From / By Ruan Bekker https://github.com/ruanbekker

https://github.com/ruanbekker/grafana-observability-primer

## Environment variables:

```java

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/grafana-observability-primer-prometheus-k6-load-testing.git
git push -u origin main
```

## Results

Flask API http://localhost:5000/users

Grafana http://localhost:3000/d/j0VZzcy7z/application-metrics?orgId=1&from=now-15m&to=now

# grafana-observability-primer

Grafana Observability Primer

## stack

Deploy:

```bash
docker-compose up -d --build
```

## k6

Create user:

```bash
docker run --rm -i --network=docknet loadimpact/k6 run --quiet - < k6lib/http_post.js
```

Run tests to perform get requests:

```bash
docker run --rm -i --network=docknet loadimpact/k6 run --quiet - < k6lib/http_gets.js
```

## usage

API Usage:

```
# list all users
curl -H 'Content-Type: application/json' http://localhost:5000/users
```

```
# create user
curl -XPOST -H 'Content-Type: application/json' http://localhost:5000/users -d '{"username": "ruan", "email": "ruan@localhost"}'
```

## grafana screenshots

CPU and Memory:

![image](https://user-images.githubusercontent.com/567298/160496251-76fea7a6-11fa-419c-a9fc-2f9b2c2f2604.png)

Requests per Second:

![image](https://user-images.githubusercontent.com/567298/160496321-3b42bdf3-ce19-4c68-b0bd-4961c9fac24c.png)

Average Response Time:

![image](https://user-images.githubusercontent.com/567298/160496357-08a0d009-265f-4cd7-ad02-635d7e1d58f1.png)

Response Duration:

![image](https://user-images.githubusercontent.com/567298/160496393-8a65a499-882a-49ad-8f7d-1157fff4063a.png)
