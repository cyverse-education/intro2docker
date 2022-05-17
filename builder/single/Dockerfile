FROM golang:latest
WORKDIR /go/src/app
ADD . /go/src/app
RUN go mod init
RUN cd /go/src/app && go build -o hello
ENTRYPOINT ./hello
