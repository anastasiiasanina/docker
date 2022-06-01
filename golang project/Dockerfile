FROM golang:1.18.2-buster as build 

WORKDIR /app

COPY . .

RUN CGO_ENABLED=0 go build -o build/fizzbuzz

FROM gcr.io/distroless/static

COPY --from=build /app/build/fizzbuzz /app/fizzbuzz

CMD ["./build/fizzbuzz", "serve"] 