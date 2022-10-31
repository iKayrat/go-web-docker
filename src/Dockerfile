FROM golang:alpine
# RUN go get github.com/astaxie/beego
# RUN go get github.com/beego/bee
# ENV G0111MODULE=on
ENV GOPATH=/
# ADD go.mod .
# ADD go.sum .
WORKDIR /app

COPY go.mod ./
COPY go.sum ./

RUN go mod download

COPY ./ ./

# ENV GOFLAGS=-mod=vendor

# USER $APP_USER
RUN go build -o /src

CMD ["/src"]