# Quarkus Continuous Testing
Quarkus enhances productivity and efficiency, allowing developers to focus on writing high-quality code.

- **Write Any Java Code**:
  - Quarkus supports simple standard Java code, enabling developers to utilize familiar programming paradigms and libraries.
    
- **Live Reload**:
  - With Quarkus, changes made to your code are automatically detected, and your application is reloaded instantly. This feature allows for rapid iteration and testing, making the development process smoother and faster.

- **Continuous Testing**:
  - Quarkus provides a robust testing framework that runs your tests automatically every time you make a change to your code. This ensures that you receive immediate feedback on the impact of your changes, helping you catch issues early in the development cycle.

- **Minimal dependencies**
  - This project has only ARC (Quarkus Dependency Injection Containter) and Junit5 dependencies. Dependency injection is not used.


## Getting Started
To start using Quarkus with Live Reload and Continuous Testing, run the following command in your terminal and use the CLI menu options:

```bash
mvn quarkus:dev

```

## Packaging and running the application
The application can be packaged using:

```shell script
./mvnw package
```

It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:

```shell script
./mvnw package -Dquarkus.package.jar.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable
You can create a native executable using:

```shell script
./mvnw package -Dnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/code-with-quarkus-1.0.0-SNAPSHOT-runner`
