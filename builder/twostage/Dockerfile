# build stage
FROM golang:latest AS build-env
WORKDIR /go/src/app
ADD . /go/src/app
RUN go mod init
RUN cd /go/src/app && go build -o hello

# second (final) stage
FROM alpine:latest
WORKDIR /app
COPY --from=build-env /go/src/app /app/
ENTRYPOINT ./hello
