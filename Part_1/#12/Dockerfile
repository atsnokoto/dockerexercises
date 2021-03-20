
FROM ubuntu:16.04
EXPOSE 5000

WORKDIR /usr/src/app
COPY example-frontend .


# INSTALL PREREQUISITES
RUN apt update && apt install -y curl && curl -sL https://deb.nodesource.com/setup_14.x | bash && apt install -y nodejs
RUN node -v && npm -v

RUN npm install

# STARTING IN PRODUCTION MODE
RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
