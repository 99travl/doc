# System requirements

This project is a microservice which is
called by other services and is calling
other services. So we stub as interfaces
to be implemented by other services.

Each service need the same requirements
to be up and running normally.

These are following:

| Project  | Dev. Env              | Prod             | Test   | Integration test |
|----------|-----------------------|------------------|--------|------------------|
| Messages | JDK 17, Maven, Docker | JRE 17 or Docker | JDK 17 | JDK 17, Docker   |
| 99Travl  | JDK 17, Maven, Docker | JRE 17 or Docker | JDK 17 | JDK 17, Docker   |
| Payments | JDK 17, Maven, Docker | JDK 17 or Docker | JDK 17 | JDK 17, Docker   |

As show upper, we use these services:

- [JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html).
  I personally use [sdkman](https://sdkman.io/)
  to manage all versions of Java installed.
- [Maven](https://maven.apache.org/install.html)
  to manage dependencies when working with
  multiple Java Repositories. I personally
  also use [sdkman](https://sdkman.io/) to
  manage all versions of maven and update it.
- [Docker](https://docs.docker.com/engine/install/)
  to create and run virtual machines rapidly.
  We use it to deploy easily our dependencies
  for the core app.

Not written there, but for the development,
you'll need to have a code editor to simply
tasks.

These apps can run on ***any CPU*** that Java accepts.

Now these services are used by the whole
system to ensure the complete service:

| Project  | Usage                                                                                                              | Prod Requirements |
|----------|--------------------------------------------------------------------------------------------------------------------|-------------------|
| Messages | For chatting, sending & receiving <br/>message through all apps managed <br/>in this system.                       | JRE 17 or Docker  |
| 99Travl  | For managing people's travels and parcels.                                                                         | JRE 17 or Docker  |
| Payments | For making payments, saving them <br/>and sync with other apps.                                                    | JDK 17 or Docker  |
| Keycloak | This one alone manages all the <br/>security, authentication and authorization.                                    | Docker            |
| RabbitMQ | This messaging broker is used to <br/>send messages to other services.                                             | Docker            |
| Redis    | This NoSQL database is used for <br/>caching purpose. It makes request faster <br/>and the whole system also fast. | Docker            |
| DB       | The Database is used to persist <br/>things in. They are attached to each <br/>service.                            | Docker            |

The next step is [Run the project](./run.md).