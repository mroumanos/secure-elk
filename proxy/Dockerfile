FROM golang

WORKDIR /go/src/app

RUN go get github.com/bitly/oauth2_proxy

ADD config/oauth2.cfg oauth2.cfg

EXPOSE 4180

CMD [ "oauth2_proxy", "-config=/go/src/app/oauth2.cfg" ]