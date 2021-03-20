
FROM golang:1.15

EXPOSE 8080

WORKDIR /apps
COPY example-backend .

RUN go build

ENV FRONT_URL=http://localhost:8080

CMD ["./server"]

