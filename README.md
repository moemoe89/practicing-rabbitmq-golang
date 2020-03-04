# PRACTICING-RABBITMQ-GOLANG #

Practicing RabbitMQ Using Golang with Go Mod as Programming Language, RabbitMQ as Messaging

## Directory structure
Your project directory structure should look like this
```
  + your_gopath/
  |
  +--+ src/github.com/moemoe89
  |  |
  |  +--+ practicing-rabbitmq-golang/
  |     |
  |     +--+ consumer
  |        |
  |        +--+ config/
  |        +--+ main.go
  |        +--+ ... any other source code
  |     +--+ producer
  |        |
  |        +--+ config/
  |        +--+ main.go
  |        +--+ ... any other source code
  |
  +--+ bin/
  |  |
  |  +-- ... executable file
  |
  +--+ pkg/
     |
     +-- ... all dependency_library required

```

## Requirements

Go >= 1.11

## Setup and Build

* Setup Golang <https://golang.org/>
* Setup RabbitMQ <https://www.rabbitmq.com/>
* Under `$GOPATH`, do the following command :
```
$ mkdir -p src/github.com/moemoe89
$ cd src/github.com/moemoe89
$ git clone <url>
$ mv <cloned directory> practicing-rabbitmq-golang
```

## Running Application
Make config file inside producer & consumer dir :
```
$ cp config-sample.json config.json
```
Change RabbitMQ address & collection based on your config :
```
amqp://guest:guest@rabbitmq:5672/
```
Build producer / consumer inside dir :
```
$ go build
```
Run producer / consumer inside dir :
```
$ go run main.go
```

## How to Run RabbitMQ with Docker
Make config file for docker :
```
$ cp config-sample.json config.json
```
Change RabbitMQ address & collection based on your docker config :
```
amqp://guest:guest@rabbitmq:5672/
```
Build
```
$ docker-compose build
```
Run
```
$ docker-compose up
```
Stop
```
$ docker-compose down
```
Run producer / consumer inside dir :
```
$ go run main.go
```