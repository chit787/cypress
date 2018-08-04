FROM cypress/base:centos7
ADD ../cypress /tmp/source
WORKDIR /tmp/source
RUN npm install --save-dev cypress
RUN $(npm bin)/cypress verify
RUN $(npm bin)/cypress run