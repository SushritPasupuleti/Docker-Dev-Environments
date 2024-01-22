FROM golang:alpine

WORKDIR /app

ADD . /app

# Check if the files are copied
# RUN ls -la

RUN go mod download

# CMD ["go", "run", "main.go"]
ENTRYPOINT ["go", "run", "main.go"]
