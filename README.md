# ELK elastic stash

This show how multiple containers can aggregate log to logging infrastructure with docker compose using logstash, elastic search and kibana

## Run

you will need docker installed in your computer, after it :

1. Run
```
docker-compose up
```
2. Wait for kibana (this might take a bit)
3. Add logstash-* as index with @timestamp as Time-field name
4. run to get some logs from httpd
```
repeat 10 curl http://localhost:80/ 
```
5. Go to Discover 

## Architecture

the target architecture would be to allow gathering information from applications but also sync with hadoop to enable having a data lake to improve analytics, and pull directly from google analytics to logstash.

![target arch](https://user-images.githubusercontent.com/3071208/41835050-743623ce-7856-11e8-8a6b-3b0b20879d7d.png)

current architecture is 

## TODO
- [] add import fron google analytics through logstash and http_poller
- [] Add hadoop infrastructure for data analytics extension

## References & further readings

- [docker logging article](https://docs.fluentd.org/v0.12/articles/docker-logging-efk-compose) 
- [gist eunomie](https://gist.github.com/eunomie/e7a183602b8734c47058d277700fdc2d) 
- [http poller](https://www.elastic.co/guide/en/logstash/current/plugins-inputs-http_poller.html)
- [hadoop elastic search](https://www.elastic.co/products/hadoop)
- [hadoop vs elastic search](https://blog.treasuredata.com/blog/2015/08/31/hadoop-vs-elasticsearch-for-advanced-analytics/)