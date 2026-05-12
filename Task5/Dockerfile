FROM quay.io/projectquay/golang:1.26 AS builder

WORKDIR /app
COPY . .

# Збираємо бінарник для хостової платформи/архітектури
RUN go build -o kbot .

FROM alpine:3.19
WORKDIR /app
COPY --from=builder /app/kbot .

CMD ["./kbot", "test"]
