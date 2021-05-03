# java-optimize

Optimize your Java applications for deployment

## Dockerfiles

- Use multi-stage builds
- Run the jar using the JarLauncher
- Layertools to divide into layers

## Cloud Native Buildpacks

- detect application type and dependencies
- create layers automatically
- optimize image layers
- maven or gradle commands `mvn spring-boot:build-image` and `gradle bootBuildImage`
- custom layers with `layers.idx`

## Java in K8's

- Add checks not only the container is running but also if the application is running as expected.
    - Spring Boot has actuator endpoints at `/actuator/health/liveness` and `/actuator/health/readiness`
    - Spring Boot also includes `AvailibilyState` and `AbilityChangeEvent` to trigger restarts and LoadBalancer switches
- enable gracefully server shutdowns for Spring Boot, open the `application.property` file and update `server.shutdown=graceful`

### Resources

https://www.youtube.com/watch?v=wBtUIkMgzU8
