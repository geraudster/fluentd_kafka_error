# Fluentd / Kafka input issue

Reproduce:

```
docker-compose up -d
```

Watch fluentd logs:

```
docker-compose logs -f td-agent
```

The container should stop:
```
td-agent_1   | 2021-03-01 14:44:53 +0000 [error]: #0 Using snappy compression requires adding a dependency on the `snappy` gem to your Gemfile. path=nil error_class=LoadError error="Using snappy compression requires adding a dependency on the `snappy` gem to your Gemfile."
td-agent_1   |   2021-03-01 14:44:53 +0000 [error]: #0 suppressed same stacktrace
td-agent_1   | 2021-03-01 14:44:53 +0000 [info]: fluent/log.rb:329:info: Worker 0 finished unexpectedly with status 2
td-agent_1   | 2021-03-01 14:44:53 +0000 [info]: fluent/log.rb:329:info: Received graceful stop
```

Clean all:

```
docker-compose down -v
```
