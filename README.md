# Angular Spring Boot monorepo

illustrates how to set up a spring and angular project in one repo

## Usage

the default task on the root project is to run the backend, so just:

```shell
./gradlew
```

and then open your browser to [http://localhost:8080](http://localhost:8080).

## Implementation

basically, the interesting parts of this repo are the [backend](./backend/build.gradle) and [frontend](./frontend/build.gradle) `build.gradle`s.

## Project Setup

bootstrapped with:

```shell
gradle init wrapper \
    --gradle-version 7.5.1 \
    --distribution-type all \
    --type java-application \
    --test-framework junit-jupiter
```

and then:
```shell
(cd backend && \
    spring init -d web --build gradle --format build)
```

and the frontend, with:

```shell
(cd frontend && \
    NG_CLI_ANALYTICS=ci \
    ng \
    --name frontend \
    --commit false \
    --directory . \
    --interactive false \
    --package-manager npm \
    --routing \
    --skip-git \
    --style css \
    new 
)
```
