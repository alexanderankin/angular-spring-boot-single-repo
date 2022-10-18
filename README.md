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
