# ![logomakr_5axvtc](https://user-images.githubusercontent.com/3071208/41837679-81e03624-785e-11e8-841c-4bd25a61b5cd.png)

This show how multiple containers can aggregate log to logging infrastructure with docker compose using logstash, elastic search and kibana

## Run

you will need docker installed in your computer, after it :

1. Run
```zsh
docker-compose up
```
2. Wait for kibana (this might take a bit)
3. Add logstash-* as index with @timestamp as Time-field name
4. run to get some logs from httpd
```zsh
repeat 10 curl http://localhost:80/ 
```
5. Go to Discover 

## Architecture

the target architecture would be to allow gathering information from applications but also sync with hadoop to enable having a data lake to improve analytics, and pull directly from google analytics to logstash.

![41835539-452a2704-7858-11e8-994d-0943039758fe](https://user-images.githubusercontent.com/3071208/41849145-2e0f2ee8-7880-11e8-9580-9fd0c1aa31fd.png)

(current architecture is missing google analytics and hadoop as seen in TODO list)

## Backlog
- [X] Add kibana container
- [X] Add elasticsearch container
- [X] Add logstash container and configuration
- [X] Add aplication containers
- [ ] Add import fron google analytics through logstash and http_poller
- [ ] Add hadoop infrastructure for data analytics extension

## References & further readings

- [docker logging article](https://docs.fluentd.org/v0.12/articles/docker-logging-efk-compose) 
- [gist eunomie](https://gist.github.com/eunomie/e7a183602b8734c47058d277700fdc2d) 
- [http poller](https://www.elastic.co/guide/en/logstash/current/plugins-inputs-http_poller.html)
- [hadoop elastic search](https://www.elastic.co/products/hadoop)
- [hadoop vs elastic search](https://blog.treasuredata.com/blog/2015/08/31/hadoop-vs-elasticsearch-for-advanced-analytics/)

### Logo

Check out the new logo that I created on <a href="http://logomakr.com" title="Logo Makr">LogoMakr.com</a> https://logomakr.com/5axvTc
