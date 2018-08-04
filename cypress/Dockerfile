FROM cypress/base:centos7
ADD . /tmp/cypress
RUN cp /tmp/cypress/cypress.json /tmp/cypress.json
WORKDIR /tmp
RUN npm install --save-dev cypress
RUN $(npm bin)/cypress verify
RUN $(npm bin)/cypress run