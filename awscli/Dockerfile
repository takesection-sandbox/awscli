FROM python:3.7-buster

RUN apt-get update \
  && apt-get upgrade -y \
  && curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip" \
  && unzip awscli-bundle.zip \
  && ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws \
  && rm -f awscli-bundle.zip \
  && rm -rf awscli-bundle

CMD ["/usr/local/bin/aws"]

