FROM golang:1.18-alpine

RUN mkdir /app

RUN addgroup -S zellgroup
RUN adduser -S -D -h /app zelluser zellgroup
RUN chown -R zelluser:zellgroup /app
USER zelluser

COPY main.go /app

EXPOSE 8080
CMD go run /app/main.go
