FROM adminer

EXPOSE 8080

# Switch current user to root to have permission to run commands
USER root

RUN apk update && \
	apk add autoconf openssl-dev g++ make && \
    apk del --purge autoconf openssl-dev g++ make
