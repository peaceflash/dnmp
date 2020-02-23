ARG NODE_VERSION
FROM ${NODE_VERSION}


ARG TZ
ARG NODE_VERSION
ARG CONTAINER_PACKAGE_URL

RUN if [ "${CONTAINER_PACKAGE_URL}" != "" ]; then \
        sed -i "s/dl-cdn.alpinelinux.org/${CONTAINER_PACKAGE_URL}/g" /etc/apk/repositories; \
    fi
RUN apk --no-cache add vim 
RUN apk --no-cache add make gcc g++ python

RUN npm install -g cnpm --registry=https://registry.npm.taobao.org
RUN cnpm install -g @vue/cli
WORKDIR /nodesrc/

