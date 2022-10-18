# Angular Spring Boot monorepo

illustrates how to set up a spring and angular project in one repo

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
