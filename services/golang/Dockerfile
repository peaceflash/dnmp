ARG GOLANG_VERSION
FROM ${GOLANG_VERSION}


ARG TZ
ARG GOLANG_VERSION
ARG CONTAINER_PACKAGE_URL

RUN if [ "${CONTAINER_PACKAGE_URL}" != "" ]; then \
        sed -i "s/dl-cdn.alpinelinux.org/${CONTAINER_PACKAGE_URL}/g" /etc/apk/repositories; \
    fi
RUN apk --no-cache add vim 


WORKDIR /go/

