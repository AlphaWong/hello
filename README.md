# Objective
Testing ktor is a good web framework or not and the size of the docker image.
I am happy to share my result.

# test
```console
docker build -f ./Dockerfile.alpine -t my-application:alpine .
docker build -f ./Dockerfile.distroless -t my-application:distroless .
```

# Result
```console
NAME             IMAGE                      HASH           SIZE
my-application   openjdk:8-jre-alpine       4142a795c924   140MB
my-application   gcr.io/distroless/java:8   b00bb8b7045d   100MB
```

# Sum up
1. I think better to follow the ktor tutorial
1. gradle will have permission issue

# Reference
1. Google distroless (https://github.com/GoogleContainerTools/distroless/blob/master/examples/java/Dockerfile)
1. Ktor tutorial (https://ktor.io/quickstart/quickstart/docker.html#prepare-docker-image)

# Question
ask me @ `alpha.wong@tuta.io`