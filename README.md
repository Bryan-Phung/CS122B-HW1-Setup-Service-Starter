# CS122B Homework 1 - The Setup Service

#### [Config](#config)

## Config
##### `application.yml`

```yml
spring:
  application:
    name: SetupService

server:
  address: 0.0.0.0
  port: 10010
  error: # These settings are for debugging
    include-exception: true
    include-message: always 

logging:
  file:
    name: ./SetupService.log
```