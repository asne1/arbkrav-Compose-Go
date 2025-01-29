FROM golang:1.20-alpine

WORKDIR /app

# Kopier go.mod og go.sum og installer avhengigheter
COPY go.mod ./
COPY go.sum ./
RUN go mod download

# Kopier resten av kildekoden
COPY *.go ./

# Bygg binærfilen
RUN go build -o /api

EXPOSE 8080

CMD ["/api"]