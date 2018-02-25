# README

## Features

Write some features...

## System dependencies

 - mysql
 - td-agent

## Configuration

### td-agent

It requires td-agent installed at local for "act-fluent-logger-rails" gem.
An example of td-agent.conf follows.

```
<filter rails>
  @type parser
  key_name messages
  <parse>
    @type json
  </parse>
</filter>

<filter rails>
  @type record_transformer
  remove_keys location 
</filter>

<match rails>
  @type copy
  <store>
    @type stdout
  </store>
</match>
```


Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
