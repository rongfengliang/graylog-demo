# graylog with new version for upgrade test

## how to test

> upgrage  2.4.5-1 to 3.1.2

* start  2.4.5-1 &&  ingress some logs

* change  graylog version to 3.1.2 && do some test


## some notes

* for running you need  add some  hosts  config

```code
127.0.0.1 graylog
```

* gelf http input test

```code
curl -X POST -H 'Content-Type: application/json' -d '{ "version": "1.1", "host": "example.org", "short_message": "A short message", "level": 5, "_some_info": "foo" }' 'http://localhost:12201/gelf'
```


## some  links

[elasticsearch upgrade](https://www.elastic.co/guide/en/elasticsearch/reference/6.8/rolling-upgrades.html)

[graylog  upgrade](https://docs.graylog.org/en/2.5/pages/upgrade.html#upgrading-elasticsearch)