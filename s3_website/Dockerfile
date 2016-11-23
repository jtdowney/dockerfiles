FROM alpine

RUN apk --update add ruby ruby-io-console openjdk8-jre
RUN gem install --no-document s3_website
RUN s3_website install

ENTRYPOINT ["/usr/bin/s3_website"]
