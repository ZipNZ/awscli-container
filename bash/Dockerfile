#Source image is alpine
FROM alpine:3.10.2 

LABEL maintainer="Scott Murray <scottam.coder@gmail.com>"

#Install python3 in order to install AWSCLI
RUN apk update && apk add \
  python3 \
  groff \
  jq \
  bash

#Upgrade pip and install the aws cli
RUN pip3 install --upgrade pip && pip3 install awscli

CMD [ "aws" ]