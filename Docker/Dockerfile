FROM golang:1.12beta2-alpine3.8 as builder

RUN apk add --update git && \
    go get -d github.com/devcodewak/tsog_openshift/cmd  && \
    go build -ldflags="-s -w" -o /go/bin/web github.com/devcodewak/tsog_openshift/cmd


	
FROM alpine:3.8

WORKDIR /bin/

COPY --from=builder /go/bin/web .

RUN web -V

CMD ["/bin/web", "-L=http2://env:env@:8443", "-L=mws://env:env@:8444", "-N"]

EXPOSE 8443 8444