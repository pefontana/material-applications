FROM golang:1.16
WORKDIR /usr/src/app

COPY . .

RUN go build

WORKDIR /usr/src/app

COPY --from=build /usr/src/app/server .

EXPOSE 8080

CMD ["./server"]
