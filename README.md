# Installation
This project needs a postgresql running on port 5432, you can easily start with docker with below command;

```docker run --ulimit memlock=-1:-1 -it --rm=true --memory-swappiness=0 \
           --name postgres-quarkus-reactive -e POSTGRES_USER=quarkus_test \
           -e POSTGRES_PASSWORD=quarkus_test -e POSTGRES_DB=quarkus_test \
           -p 5432:5432 postgres:11.2
```
This project uses quarkus which is competible with java 11.

# getting-started-reactive-crud project

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```
# test the app
you can test the endpoints with below postman collection;

https://www.getpostman.com/collections/1e42c91504dfd7617fde

set the URL variable and you are set to test.

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/getting-started-reactive-crud-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.html.

## Related guides


## Provided examples

### RESTEasy Reactive example

Rest is easy peasy & reactive with this Hello World RESTEasy Reactive resource.

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)
