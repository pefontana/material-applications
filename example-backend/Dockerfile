FROM golang:1.16-alpine


ENV REQUEST_ORIGIN=http://localhost:5000
# ENV REQUEST_ORIGIN=http://localhost:80
EXPOSE 8080
WORKDIR /app

COPY . .

RUN go build

RUN adduser -D executor
USER executor

CMD [ "./server" ]
