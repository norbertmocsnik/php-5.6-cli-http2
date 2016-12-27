# php-5.6-cli-http2

Upgrades official php 5.6.xx-cli docker image to support outgoing http2 curl calls

Same as offical https://hub.docker.com/_/php/ 5.6.xx-cli docker image with these changes in Dockerfile:
* instead of building FROM debian:jessie it builds FROM norbertm/debian-curl-http2:latest which adds http2 support to curl in debian (see https://github.com/norbertmocsnik/debian-curl-http2)
* curl & libcurl4-openssl-dev install was removed since it already exists in a newer version
* added libssh2-1-dev which becomes then a dependency

Also available on Docker Hub: https://hub.docker.com/r/norbertm/php-5.6-cli-http2/
