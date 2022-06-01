FROM golang:1.18.2-buster

WORKDIR /app

COPY go.mod go.sum ./
COPY . .

RUN go mod download
RUN go build -o build/fizzbuzz

CMD ["./build/fizzbuzz", "serve"] 