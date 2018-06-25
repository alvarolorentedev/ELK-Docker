# ELK elastic stash
a logging infrastructure with docker compose using logstash, elastic search and kibana

## Run

you will need docker installed in your computer, after it :
1. Run
```
docker-compose up
```
2. Wait for kibana to be up (this might take a bit)
3. Add logstash-* as index with @timestamp as Time-field name
4. Go to Discover and see your logs!