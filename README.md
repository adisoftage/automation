<img src="https://netflix.github.io/Hystrix/images/hystrix-logo-tagline-850.png">

# Hystrix Status
Hystrix is no longer in active development, and is currently in maintenance mode.

Hystrix is stable enough to meet the needs of Netflix for our existing application. Meanwhile, our focus has shifted towards more adaptive implementations that react to an application's real time performance rather than pre-configured settings (for example, through [adaptive concurrency limits](https://medium.com/@NetflixTechBlog/performance-under-load-3e6fa9a60581)). For the cases where something like Hystrix makes sense, we intend to continue using Hystrix for existing applications, and to leverage open and active projects like [resilience4j](https://github.com/resilience4j/resilience4j) for new internal projects. We are the beginning to recommend others do the same.

Hystrix has served Netflix and the community well over the years, and the transition to maintenance mode is in no way an indication that the concepts and ideas from Hystrix are no longer valuable. On the contrary, Hystrix has inspired many great ideas and projects. we thank everyone at Netflix, and in the greater community, for all the contributions made to hystrix over the years.

## Introduction

Hystrix is a latency and fault tolerance library designed to isolate points of access to remote systems, services and 3rd party libraries, stop cascading failure and enable resilience in comple distributed systems where failure is inevitable.

## Full Documentation

see the [Wiki](https://github.com/Netflix/Hystrix/wiki/) for full documentation, example , operational details and other information.

See the [Javadoc](https://netflix.github.com/Hystrix/javadoc) for the API.


## Communication

- Google Group: [HystrixOSS](https://groups.google.com/d/forum/hystrixoss)
- Twitter: [@HystrixOSS](https://twitter.com/HystrixOSS)
- [GitHub Issues](https://github.com/Netflix/Hystrix/issues)

## What does it do?

### 1) Latency and Fault Tolerance 

Stop cascading failures. Fallbacks and graceful degradation. Fail fast and rapid recovery.

Thread and semaphore isolation with circuit breakers.

### 2) Realtime Operations

Realtime monitoring and configuration changes. Watch service and property changes take effect immediately as they spread across a fleet.

Be alerted, make decisions, affect change and see results in seconds.


More examples and information can be found in the [How to Use](https://github.com/Netflix/Hystrix/wiki/How-To-Use) section

Example source code can be found in the [hystrix-examples](https://github.com/Netflix/Hystrix/tree/master/hystrix-examples/src/main/java/com/netflix/hystrix/examples) module.

change history and version numbers => [CHANGELOG.md](https://github.com/Netflix/Hystrix/blob/master/CHANGELOG.md)

To build:

```
$ git clone git@github.com:Netflix/Hystrix.git
$ cd Hystrix/
$ ./gradlew build
```

## Run Demo
To run a [demo app](https://github.com/Netflix/Hystrix/tree/master/hystrix-examples/src/main/java/com/netflix/examples/demo/HystrixCommandDemo.java) do the following:

```

$ git clone git@github.com:Netflix/Hystrix.git
$ cd Hystrix/
./gradlew runDemo
```

## Dashboard

The hystrix-dashboard component of this project has been deprecated and moved to [Netflix-Skunkworks/hystrix-dashboard](https://github.com/Netflix-Skunkworks/hystrix-dashboard). Please see the README there for more details including important security considerations.

## Bugs and Feedback

For bugs, questions and discussions please use the [Github Issues](https://github.com/Netflix/Hystrix/issues).
