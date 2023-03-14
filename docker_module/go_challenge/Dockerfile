FROM golang:alpine AS builder
WORKDIR /app
COPY go.mod main.go ./
RUN go build main.go

FROM alpine
WORKDIR /app
COPY --from=builder /app/main .
CMD [ "./main" ]