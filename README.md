# Saga [![Build Status](https://travis-ci.org/ServiceComb/ServiceComb-Saga.svg?branch=master)](https://travis-ci.org/ServiceComb/ServiceComb-Saga?branch=master) [![Coverage Status](https://coveralls.io/repos/github/ServiceComb/ServiceComb-Saga/badge.svg?branch=master)](https://coveralls.io/github/ServiceComb/ServiceComb-Saga?branch=master) [![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

## Purpose
Saga is a type of Compensating Transaction pattern, which provides a simple way to help users solve the data consistency problems encountered in micro-service applications.

## Documentation
Reference documentation is available on the [ServiceComb website][servicecomb-website].

[servicecomb-website]: http://servicecomb.io/

## Major Architecture of Saga
* saga-core(transaction and compensation handling logic)
* saga-format(data serialization and deserialization)
* saga-transports(communication protocol implementation such as rest or rpc in the future)
* saga-discovery(service discovery)
* saga-spring(restful service framework)

![Saga](docs/static_files/saga.png) 

## Prerequisites
You will need:
1. [Oracle JDK 1.8+][jdk]
2. [Maven 3.x][maven]
3. [Docker][docker]
4. [MySQL][mysql]
5. [Service Center(optional)][service_center]
6. [Docker compose(optional)][docker_compose]
7. [Docker machine(optional)][docker_machine]


[jdk]: http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
[maven]: https://maven.apache.org/install.html
[docker]: https://www.docker.com/get-docker
[mysql]: https://dev.mysql.com/downloads/
[service_center]: https://github.com/ServiceComb/service-center
[docker_compose]: https://docs.docker.com/compose/install/
[docker_machine]: https://docs.docker.com/machine/install-machine/



## Building
Download the source code.
```
git clone https://github.com/ServiceComb/saga.git
```

Enter the Saga root directory,biuld Saga project by maven command and generate a docker image named saga-spring in local.
```
mvn package -DskipTests -Pdocker
```

## Run Services
A `docker-compose.yaml` file is provided to start Saga services and its dependencies(Service center and Mysql) as docker containers.
User also can configure specified Service center or Mysql in `docker-compose.yaml`.

Enter the Saga root directory, run all service images using command,
```
docker-compose up
```


## Reference API
See [Saga API](docs/api/api.md) for details.


## Example
See [Saga demo](https://github.com/ServiceComb/ServiceComb-Saga/tree/master/saga-demo) for details.

## Contact
Bugs: [issues](https://github.com/ServiceComb/saga/issues).

Mailing lists: [subscribe](mailto:dev-subscribe@servicecomb.incubator.apache.org) 

## Contributing
See [Pull Request Guide](http://servicecomb.io/developers/submit-codes/) for details.

## Reporting Issues
See reporting bugs for details about reporting any issues.
