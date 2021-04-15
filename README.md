This repository bundles Ceres projects as submodules

## Cloning the bundle

```
git clone --recursive git@github.com:racker/ceres-bundle.git
```

## Structure

Directory | Description
----------|------------
[apps](apps) | contains the core production applications
[test](test) | contains modules for testing

## Quickstart

[install docker](https://docs.docker.com/get-docker/) if you don't already have it installed

create required application infrastructure:
```
cd test/infrastructure
docker-compose up -d main
```

for each of the `apps` modules, start the application in a new terminal:
```
cd apps/app
mvn spring-boot:run
```

generate metrics data:
```
cd test/data-generator
mvn spring-boot:run
```
