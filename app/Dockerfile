FROM golang:1.21.3

MAINTAINER Quentin Ragoucy

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download && go mod verify

COPY main.go .
RUN go build -v -o sre-hiring

EXPOSE 8080

CMD ["/app/sre-hiring"]