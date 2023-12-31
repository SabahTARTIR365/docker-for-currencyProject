# Docker

## Images

- https://hub.docker.com/u/11716265
- Currency Exchange Service 
	- 11716265/mmv3-currency-exchange-service:0.0.1-SNAPSHOT
- Currency Conversion Service
	- 11716265/mmv3-currency-conversion-service:0.0.1-SNAPSHOT
- Eureka
	- 11716265/mmv3-naming-server:0.0.1-SNAPSHOT
- API GATEWAY
	- 11716265/mmv3-api-gateway:0.0.1-SNAPSHOT

## URLS

#### Currency Exchange Service
- http://localhost:8000/currency-exchange/from/USD/to/INR

#### Currency Conversion Service
- http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8100/currency-conversion-feign/from/USD/to/INR/quantity/10

#### Eureka
- http://localhost:8761/

#### Zipkin
- http://localhost:9411/

#### API GATEWAY
- http://localhost:8765/currency-exchange/from/USD/to/INR
- http://localhost:8765/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-feign/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-new/from/USD/to/INR/quantity/10

#### Commands
```
docker run -p 9411:9411 openzipkin/zipkin:2.23
docker push docker.io/11716265/mmv3-currency-exchange-service:0.0.1-SNAPSHOT
docker-compose --version
docker-compose up
docker push 11716265/mmv3-naming-server:0.0.1-SNAPSHOT
docker push 11716265/mmv3-currency-conversion-service:0.0.1-SNAPSHOT
docker push 11716265/mmv3-api-gateway:0.0.1-SNAPSHOT
watch -n 0.1 curl http://localhost:8000/sample-api
```
