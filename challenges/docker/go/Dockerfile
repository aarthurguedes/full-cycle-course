FROM golang:1.20-alpine AS build

WORKDIR /app

COPY go.mod ./
COPY main.go ./

RUN go build -o /full-cycle-rocks

FROM scratch

COPY --from=build /full-cycle-rocks /full-cycle-rocks

ENTRYPOINT [ "/full-cycle-rocks" ]
